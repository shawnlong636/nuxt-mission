<template>
  <div class="container">
    <NuxtLogo />
    <h1 class="title">Nuxt Mission</h1>
    <button @click="showPlanets">{{ show ? 'Hide' : 'Show' }} Planets</button>
    <div v-if="show">
      <LazyPlanetsList />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  layout: 'home',
  data() {
    return {
      show: false,
    }
  },
  methods: {
    showPlanets() {
      this.show = !this.show
    },
  },
})
</script>

<style scoped lang="scss">
.container {
  display: grid;
  justify-items: center;
  margin: 0 auto;
  text-align: center;

  & > ul {
    margin: 0;
    padding: 0;
  }

  & li {
    padding-bottom: 0.5em;
    margin: 0;
  }
}
</style>
