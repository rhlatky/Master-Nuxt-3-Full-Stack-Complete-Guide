<template>
  <div class="flex space-x-2 items-center">
    <div class="text-gray-500 text-xs" v-if="showNextModeLabel">change to {{nextMode}}</div>
    <button
        class="hover:bg-gray-200 dark:hover:bg-gray-600 px-2 py-1 text-gray-500"
        @mouseenter="showNextModeLabel = true"
        @mouseleave="showNextModeLabel = false"
        @click="toggleMode">
      {{ nextModeIcon }}
    </button>
  </div>
</template>

<script setup lang="ts">
const colorMode = useColorMode();

const modes = ['system', 'light', 'dark']
const nextModeIcons: {[key: string]: string} = {
  system: '🌓',
  light: '🌕',
  dark: '🌑'
}

const nextMode = computed(() => {
  const currentModeIndex = modes.indexOf(colorMode.preference);
  let nextModeIndex = null;
  if (currentModeIndex + 1 === modes.length) {
    nextModeIndex = 0;
  } else {
    nextModeIndex = currentModeIndex + 1;
  }

  return modes[nextModeIndex];
})

const toggleMode = () => {
  colorMode.preference = nextMode.value;
}

const nextModeIcon = computed(() => nextModeIcons[nextMode.value])
const showNextModeLabel = ref(false)
</script>

<style scoped>

</style>