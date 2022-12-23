<template>
  <div class="container">
    <NuxtLogo />
    <h1>About</h1>
    <p>This is the about page. Information about the page goes here.</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  head() {
    return {
      title: 'About',
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: 'https://jamstack-explorers-nuxt-mission/about',
        },
      ],
    }
  },
})
</script>

<style lang="scss">
.container {
  display: grid;
  justify-items: center;
}
</style>
