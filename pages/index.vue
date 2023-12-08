<template>
  <div>
    <h1>Welcome to the homepage</h1>
  </div>
</template>

<script lang="ts" setup>
useSeoMeta({
  title: 'Main page',
  description: 'description of the main page',
  ogTitle: 'Main page',
  ogDescription: 'description of the main page',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: 'Main page',
  twitterDescription: '[twitter:description]',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary',
});

useHead({
  htmlAttrs: {
    lang: 'en',
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png',
    },
  ],
});
</script>
