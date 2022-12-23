<template>
  <div>
    <Nuxt />
    <nav class="home-nav">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
    </nav>
  </div>
</template>

<style scoped>
.home-nav {
  justify-content: center;
}
</style>
