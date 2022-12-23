<template>
  <div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
    </nav>
    <Nuxt />
  </div>
</template>

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
