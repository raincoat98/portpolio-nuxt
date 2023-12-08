<script lang="ts" setup>
const colorMode = useColorMode();

console.log(colorMode.preference);
colorMode.preference = 'light';

useHead({
  titleTemplate: '%s - Nuxt.js',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com',
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
      crossorigin: '',
    },
  ],
});
</script>

<template>
  <div class="container mx-auto">
    <main class="p-2 mt-10">
      <Header
        class="flex items-center justify-between py-4 mb-8 border-b-2 border-gray-100"
      >
        <div class="flex items-center space-x-12">
          <div>
            <nuxt-link to="/" class="text-2xl '">Nuxt.js</nuxt-link>
          </div>

          <Menu />
        </div>

        <ClientOnly>
          <ColorModeSelector />
        </ClientOnly>
      </Header>
      <slot />
    </main>
  </div>
</template>

<style>
body {
  font-family: 'Roboto', sans-serif;
}

body {
  @apply bg-white dark:bg-gray-800 text-gray-700 dark:text-gray-300;
}
</style>
