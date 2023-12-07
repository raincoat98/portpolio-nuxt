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
<div class="container mx-auto">
    <Header class="
      flex
      items-center
      justify-between
      py-4
      mb-8
      border-b-2
      border-gray-100
    ">
      <span>
        <nuxt-link to="/" class="
        text-2xl
        '">Nuxt.js</nuxt-link>
      </span>
        <nav>
        <nuxt-link to="/" class="
          mr-4
          text-sm
          hover:bg-gray-200
          pa-2
        ">Home</nuxt-link> |
        <nuxt-link to="/about" class="
          mr-4
          text-sm
          hover:bg-gray-200
          pa-2
        ">About</nuxt-link>
      </nav>
    </Header>
    <slot />
  </div>
</template>

<style lang="scss" scoped>
body {
  font-family: 'Roboto', sans-serif;
}
</style>