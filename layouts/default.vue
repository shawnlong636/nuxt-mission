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

<style lang="scss">
html {
  font-family: 'Source Sans Pro', 'Segoe UI', Roboto, 'Open Sans',
    'Helvetica Neue', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
}

ul {
  list-style-type: none;
  padding: 0;
}

a {
  text-decoration: none;
  color: rgb(70, 70, 70);

  &:visited {
    color: inherit;
  }

  &:hover {
    text-decoration: underline;
  }
}

nav {
  display: flex;

  & > * {
    margin: 10px;
  }
}
</style>
