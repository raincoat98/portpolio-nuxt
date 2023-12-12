<template>
  <div>
    <nav>
      <nuxt-link to="/" class="mr-4 text-sm h p-2 link">Home</nuxt-link>
      |
      <nuxt-link to="/about" class="mr-4 text-sm p-2 link">About</nuxt-link>
      |
      <nuxt-link to="/projects" class="mr-4 text-sm p-2 link">
        Project
      </nuxt-link>
      |
      <nuxt-link to="/blog" class="mr-4 text-sm p-2 link"> Blogs </nuxt-link>
    </nav>
  </div>
</template>
<style scoped>
.link {
  @apply p-1 hover:bg-gray-200 dark:hover:bg-gray-700;
}
</style>
