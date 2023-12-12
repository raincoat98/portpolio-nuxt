<template>
  <div>
    <nav>
      <ul class="flex flex-col md:flex-row md:space-x-4">
        <li>
          <nuxt-link to="/" class="mr-4 text-sm link">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about" class="mr-4 text-sm link">About</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/projects" class="mr-4 text-sm link">
            Project
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/blog" class="mr-4 text-sm link"> Blogs </nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>
<style scoped>
.link {
  @apply p-1 hover:bg-gray-200 dark:hover:bg-gray-700 text-2xl md:text-base;
}
</style>
