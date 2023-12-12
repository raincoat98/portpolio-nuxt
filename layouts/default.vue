<template>
  <div class="container mx-auto max-w-4xl">
    <header
      class="flex items-start md:items-center justify-between py-4 mb-8 border-b-2 border-gray-100"
    >
      <div class="flex items-center md:space-x-12">
        <div class="hidden md:block">
          <NuxtLink
            to="/"
            class="text-xl font-semibold p-2 hover:bg-gray-200 dark:hover:bg-gray-700"
            >Raincoat
          </NuxtLink>
        </div>
        <Menu />
      </div>

      <ClientOnly>
        <ColorModeSelector />
      </ClientOnly>
    </header>
    <slot />
  </div>
</template>

<script lang="ts" setup>
const colorMode = useColorMode();

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

<style>
body {
  font-family: 'Roboto', sans-serif;
}

body {
  @apply bg-white dark:bg-gray-800 text-gray-700 dark:text-gray-300;
}
</style>
