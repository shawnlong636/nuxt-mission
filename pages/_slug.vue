<template>
  <div class="container">
    <img :src="planet.image" alt="" />
    <h1 class="title">{{ planet.title }}</h1>
    <p>{{ planet.description }}</p>
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ params }) {
    const planet = await fetch(
      `https://api.nuxtjs.dev/planets/${params.slug}`
    ).then((res) => {
      if (res.ok) {
        return res.json()
      }
      throw new Error(res.status)
    })

    return { planet }
  },
  head() {
    return {
      title: this.planet.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.planet.description,
        },
      ],
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: `https://jamstack-explorers-nuxt-mission/${this.$route.params.slug}`,
        },
      ],
    }
  },
})
</script>

<style scoped>
* {
  font-family: Nunito, Roboto, sans-serif;
}

.container {
  display: grid;
  justify-items: center;
  justify-content: center;
}

img {
  width: 200px;
  border-radius: 15px;
}
</style>
