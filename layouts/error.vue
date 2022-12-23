<template>
  <div class="container">
    <p class="error-text">404</p>
    <div class="flex-row">
      <span>Take me &nbsp;</span>
      <NuxtLink to="/"><st>Home</st></NuxtLink>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  height: viewport;
  display: flex;
  flex-direction: column;
}

.error-text {
  font-size: 96pt;
  font-weight: bold;
  color: rgb(44 251 216);
}

.flex-row {
  display: flex;
  flex-direction: row;
  justify-items: start;
}

a {
  font-weight: bold;
}
</style>
