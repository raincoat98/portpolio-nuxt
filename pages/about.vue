<script lang="ts" setup>
definePageMeta({
  layout: 'another',
});
</script>

<template>
  <div>
    this is about page
    <article class="prose dark:prose-invert prose-h1:text-2xl">
      <ContentDoc path="/about" />
    </article>
  </div>
</template>

<style lang="scss" scoped></style>
