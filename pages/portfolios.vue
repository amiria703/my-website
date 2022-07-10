<template>
  <main>
    <Title>Portfolios</Title>
    <div>
      <NuxtLink to="https://amiria703.github.io/simple-login"><img loading="lazy" src="@/assets/simple-login.jpg" alt="Simple Login"></NuxtLink>
      <NuxtLink to="https://github.com/amiria703/simple-login">Simple Login</NuxtLink>
    </div>
    <div>
      <NuxtLink to="https://amiria703.github.io/my-website-v1"><img loading="lazy" src="@/assets/my-website-v1.jpg" alt="my-website-v1"></NuxtLink>
      <NuxtLink to="https://github.com/amiria703/my-website-v1">My Website V1</NuxtLink>
    </div>
    <div>
      <NuxtLink to="https://amiria703.vercel.app"><img loading="lazy" src="@/assets/my-website-v2.png" alt="my-website-v2"></NuxtLink>
      <NuxtLink to="https://github.com/amiria703/my-website-v2">My Website V2</NuxtLink>
    </div>
    <div>
      <NuxtLink to="https://github.com/amiria703/weather-app"><img loading="lazy" src="@/assets/weather-app.png" alt="Weather App"></NuxtLink>
      <NuxtLink to="https://github.com/amiria703/weather-app">Weather App</NuxtLink>
    </div>
    <div>
      <NuxtLink to="https://amiria703.ir"><img loading="lazy" src="@/assets/my-website-v3.png" alt="my-website-v3"></NuxtLink>
      <NuxtLink to="https://github.com/amiria703/my-website-v3">My Website V3</NuxtLink>
    </div>
    <div>
      <NuxtLink to="https://github.com/amiria703/the-holy-quran">The Holy Quran</NuxtLink>
    </div>
  </main>
</template>
<style scoped lang="scss">
main {
  div {
    display: flex;
    flex-direction: column;
    margin-bottom: 2rem;
    align-items: baseline;
    a {
      img {
        width: 9em;
      }
    }
  }
}
</style>