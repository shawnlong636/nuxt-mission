<template>
  <div class="container">
    <NuxtLogo />
    <h1 class="title">Nuxt Mission</h1>
    <p v-if="$fetchState.pending">Fetching Planets...</p>
    <p v-else-if="$fetchState.error">Error while fetching planets</p>
    <ul>
      <li><NuxtLink to="/Nuxt">Nuxt</NuxtLink></li>
      <li v-for="planet in planets" :key="planet.slug">
        <NuxtLink :to="planet.slug">{{ planet.title }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Planet from '../models/planet'

export default Vue.extend({
  layout: 'home',
  data() {
    const planets: Array<Planet> = []
    return { planets }
  },

  async fetch() {
    this.planets = (await fetch('https://api.nuxtjs.dev/planets').then((res) =>
      res.json()
    )) as Planet[]
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
