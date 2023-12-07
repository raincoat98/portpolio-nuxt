<script lang="ts" setup>
 useHead(
    {
      titleTemplate: '%s - Nuxt.js',
      link: [
        {
          rel: 'preconnect',
          href: 'https://fonts.googleapis.com'
        },
        {
          rel: 'stylesheet',
          href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
          crossorigin: ''
        }
      ]
    }
  )
</script>

<template>
  <div>
    <nav>
      <nuxt-link to="/">Home</nuxt-link> |
      <nuxt-link to="/about">About</nuxt-link>
    </nav>
    <slot />
  </div>
</template>

<style lang="scss" scoped>
body {
  font-family: 'Roboto', sans-serif;
}
</style>