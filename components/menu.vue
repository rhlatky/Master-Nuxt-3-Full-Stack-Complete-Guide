<template>
  <nav class="font-mono">
    <ul class="flex space-x-4">
      <li>
        <NuxtLink to="/" class="menu-item">Main</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about" class="menu-item">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/projects" class="menu-item">Projects</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts">

</script>

<style scoped>
.menu-item {
  @apply p-1 hover:bg-gray-200
}
</style>