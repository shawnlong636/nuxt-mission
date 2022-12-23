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
  name: 'IndexPage',
})
</script>

<style lang="scss">
.container {
  display: grid;
  justify-items: center;
}
</style>
