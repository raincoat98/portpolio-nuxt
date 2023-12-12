<template>
  <div>
    <ul>
      <li v-for="link in links" :key="link.id">
        <NuxtLink
          :to="{ path: route.path, hash: `#${link.id}` }"
          :class="{ 'ml-4': level }"
          class="hover:text-blue-500"
        >
          {{ link.text }}
        </NuxtLink>
        <TocLinks :links="link.children" :level="level + 1" />
      </li>
    </ul>
  </div>
</template>
<script setup>
const route = useRoute();
defineProps({
  links: Array,
  level: {
    type: Number,
    default: 0,
  },
});
</script>
