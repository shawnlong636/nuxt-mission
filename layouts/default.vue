<template>
  <div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
    </nav>
    <Nuxt />
  </div>
</template>
<script>
import Vue from 'vue'
export default Vue.extend({
  head: {
    title: 'Nuxt Mission',
    htmlAttrs: {
      lang: 'en',
    },
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'A mission to explore the jamstack using nuxt.',
      },
      { name: 'format-detection', content: 'telephone=no' },
    ],
  },
})
</script>
