<template>
    <div class="container mx-auto max-w-2xl">
        <header class="flex justify-between items-center mt-5">
          <div class="flex items-center space-x-12">
              <div>
                  <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">Radoslav Hlatky</NuxtLink>
              </div>
              <Menu />
          </div>
          <client-only>
            <color-mode-selector />
          </client-only>
        </header>
        <main class="p-2 mt-10">
            <slot />
        </main>
    </div>
</template>

<script setup>
useHead({
  titleTemplate: '%s - Radoslav Hlatky',
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
      crossorigin: ''
    }
  ]
})
</script>

<style>
body {
  font-family: Roboto;
  font-weight: bold;
}

body {
  @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-white
}
</style>