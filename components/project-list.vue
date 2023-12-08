<script lang="ts" setup>
const { error, pending, data } = await useFetch(
  "https://api.github.com/users/piotr-jura-udemy/repos"
);
const repos = computed(() =>
  data.value
    .filter(repo => repo.description)
    .sort((a, b) => b.stargazers_count - a.stargazers_count)
);
</script>

<template>
  <div>
    <h2 class="text-2xl font-semibold mb-10">projects page</h2>
    <section v-if="pending">
      <p>Loading...</p>
    </section>
    <section v-else-if="error">
      <p>Error: {{ error.message }}</p>
    </section>
    <section v-else>
      <ul class="grid grid-cols-1 gap-4">
        <li
          v-for="project in repos"
          :key="project.id"
          class="border border-gray-200 rounded-sm p-4 hover:bg-gray-100"
        >
          <a :href="project.html_url" target="_blank">
            <div class="flex items-center justify-between">
              <div>
                <h3 class="text-xl font-semibold">{{ project.name }}</h3>
                <span class="text-sm text-gray-500">{{
                  project.description
                }}</span>
              </div>
              <span class="text-sm text-gray-500"
                >{{ project.stargazers_count }}
              </span>
            </div>
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
