<script setup lang="ts">
import AtmosFrame from '../components/AtmosFrame.vue'
defineProps<{ kicker?: string }>()
</script>

<template>
  <AtmosFrame role="quote" :kicker="kicker"><slot /></AtmosFrame>
</template>
