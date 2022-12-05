<template>
  <div>
    <ChristmasTree v-if="size > 1" :size="size - 1" />
    <div class="flex flex-row justify-center">
      <div
        v-for="n in size"
        :key="n"
        class="relative rounded-full bg-green w-16 -m-2 h-16 flex justify-center items-center"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import ChristmasTree from './ChristmasTree.vue'
withDefaults(
  defineProps<{
    size: number
  }>(),
  {
    size: 1,
  }
)
</script>
