<script setup>
useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - amiria703` : 'amiria703';
  }
})
</script>
<template>
  <div class="root">
  <header>
    <NuxtLink to="/"><img src="/images/logo.svg" alt="Logo"/></NuxtLink>
    <div>
      <span><NuxtLink to="/whoami">$ whoami</NuxtLink></span>
      <span><NuxtLink to="/posts">myBlog();</NuxtLink></span>
      <span><NuxtLink to="/portfolios">portfolios;</NuxtLink></span>
      <span><NuxtLink to="/contact">ContactMe()</NuxtLink></span>
    </div>
  </header>
  <NuxtPage />
  <footer></footer>
  </div>
</template>
<style>
:root {
  --background-color: #2E3436;
  --text-color: #D3D7CF;
  --link-color: #8AE234;
}

* {
  box-sizing: border-box;
  scrollbar-color: #8ae234 transparent;
}

::-webkit-scrollbar {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: #8ae234;
}

body {
  margin: 0;
  user-select: none;
  font-family: monospace;
  font-size: 32px;
}


.root {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  flex-wrap: nowrap;
  margin: 9px;
  border-radius: 20px;
  background: var(--background-color);
  color: var(--text-color);
  padding: 30px;
  width: -webkit-fill-available;
  height: -webkit-fill-available;
  overflow-y: auto;
  padding-top: 0;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  background: var(--background-color);
  margin-top: 30px;
  margin-bottom: 30px;
}

header img {
  width: 3em;
  height: 3em;
  color: var(--text-color);
}

header div {
  display: flex;
  font-size: 0.6em;
}

header div > span {
  margin-left: 3em;
}

a {
  color: var(--link-color);
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
  cursor: pointer;
}
</style>
