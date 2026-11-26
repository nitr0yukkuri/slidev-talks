<script setup lang="ts">
import AtmosFrame from '../components/AtmosFrame.vue'
defineProps<{ kicker?: string }>()
</script>

<template>
  <AtmosFrame role="closing" :kicker="kicker"><slot /></AtmosFrame>
</template>
