<template>
  <div>
    Take a look at my GitHub projects
  </div>
  <section v-if="pending">Loading...</section>
  <section v-else-if="error">something went wrong</section>
  <section v-else>
    <ul class="grid grid-cols-1 gap-4">
      <li v-for="repo in data" :key="repo.id" class="border border-gray-200 rounded-sm p-4 hover:bg-gray-100 font-mono">
        <a :href="repo.html_url" target="_blank">
          <div class="flex items-center justify-between text-sm">
            <div class="font-semibold">{{ repo.name }}</div>
            <div>{{ repo.stargazers_count }} ✯</div>
          </div>
          <p class="text-sm">
            {{ repo.description }}
          </p>
        </a>
      </li>
    </ul>
  </section>
</template>

<script setup lang="ts">
import {computed} from "vue";

const {error, pending, data} = await useFetch('https://api.github.com/users/rhlatky/repos');

const repos = computed(() => data.value.sort((a, b) => b - a))
</script>

<style scoped>

</style>