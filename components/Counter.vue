<script setup lang="ts">
import { ref } from 'vue'
const count = ref(0)
</script>

<template>
  <div class="flex items-center gap-4 mt-8">
    <button class="px-4 py-2 border rounded" aria-label="Decrement" @click="count--">−</button>
    <output class="text-3xl" aria-live="polite">{{ count }}</output>
    <button class="px-4 py-2 border rounded" aria-label="Increment" @click="count++">+</button>
  </div>
</template>
