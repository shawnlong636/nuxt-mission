<template>
  <div class="container">
    <img :src="planet.image" alt="" />
    <h1 class="title">{{ planet.title }}</h1>
    <NuxtLink to="/about">About</NuxtLink>
  </div>
</template>

<script>
export default {
  async asyncData({ params }) {
    const planet = await fetch(
      `https://api.nuxtjs.dev/planets/${params.slug}`
    ).then((res) => res.json())
    return { planet }
  },
}
</script>

<style>
.container {
  display: grid;
  justify-items: start;
  justify-content: center;
}

img {
  width: 200px;
  border-radius: 15px;
}
</style>
