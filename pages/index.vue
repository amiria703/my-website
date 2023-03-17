<template>
    <main>
    <div>Hi!</div>
      <div>I am <span ref="typeWriter"></span>
        <Transition name="blink"><span v-if="typingStatus">_</span></Transition>
      </div>
    </main>
</template>

<script setup scoped>
/*
  sleep using setTimeout and promise:
*/
function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

/*
  Main text blinking:
*/
const typingStatus = ref(true);
const staticTypingCursor = ref(false);

function typingBlink() {
  if (!staticTypingCursor.value) {
    typingStatus.value = !typingStatus.value;
  } else {
    typingStatus.value = true;
  }
}

/*
  Typewriter functionality:
*/
const typeList = ref(["amiria703", "Amir Hossein Maher", "a Junior Web Developer", "a solo developer", "an open-source lover", "a programmer", "a Swiftie", "a music lover", "a student", "a lover", "a brother", "a boy"]);
const typeWriter = ref(null);

async function typeWord(word) {
  if (typeWriter.value) {
    for (let i = 0; i < word.length; i++) {
      typeWriter.value.innerText += word.charAt(i);
      await sleep(100);
    }
    staticTypingCursor.value = false;
    typingBlink();
    await sleep(5000);
    staticTypingCursor.value = true;
    typingStatus.value = true;
    for (let i = 0; i < word.length; i++) {
      typeWriter.value.innerText = typeWriter.value.innerText.substring(0, typeWriter.value.innerText.length - 1);
      await sleep(100);
    }
  } else {
    setTimeout(typeWord, 200);
  }
}

async function type() {
  for (const wordKey in typeList.value) {
    staticTypingCursor.value = true;
    await typeWord(typeList.value[wordKey] + ".").then(
        async function () {
          staticTypingCursor.value = false;
          typingBlink();
          await sleep(500);
        }
    )
  }
  type();
}

/*
  Do the thing :)
*/
onMounted(()=>{
  setInterval(typingBlink, 600);
  type();
})
</script>

<style scoped>
/*
  animations:
*/

/* blink: */
.blink-enter-active,
.blink-leave-active {
  transition: opacity 0.6s ease;
}

.blink-enter-from,
.blink-leave-to {
  opacity: 0;
}

main {
  word-break: break-all;
  font-size: 2em;
}

</style>
