<template>
  <div>
    <p v-if="$fetchState.pending">fetching planets...</p>
    <p v-else-if="$fetchState.error">Error while fetching planets</p>
    <ul v-else>
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
