<script setup lang="ts">
import AtmosFrame from '../components/AtmosFrame.vue'
defineProps<{ kicker?: string; tone?: 'light' | 'dark' }>()
</script>

<template>
  <AtmosFrame role="cover" :kicker="kicker" :tone="tone"><slot /></AtmosFrame>
</template>
