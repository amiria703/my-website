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
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  flex-wrap: nowrap;
  margin: 9px;
  border-radius: 20px;
  background: var(--background-color);
  color: var(--text-color);
  padding: 30px;
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
  flex-wrap: wrap;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
}

header img {
  width: 2em;
  color: var(--text-color);
}

header div {
  display: flex;
  font-size: 1rem;
  flex-wrap: wrap;
}

header div > span {
  margin-right: 3em;
  margin-bottom: 0.5rem;
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
