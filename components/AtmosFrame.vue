<script setup lang="ts">
withDefaults(defineProps<{
  role: 'cover' | 'content' | 'section' | 'quote' | 'code' | 'closing'
  kicker?: string
  tone?: 'light' | 'dark'
}>(), { kicker: '', tone: 'light' })
</script>

<template>
  <div class="slidev-layout atmos" :data-role="role" :data-tone="tone">
    <div class="atmos-art" aria-hidden="true">
      <div class="atmos-glow" />
      <svg class="atmos-lines" viewBox="0 0 980 552" preserveAspectRatio="xMidYMid slice" fill="none">
        <path v-for="i in 19" :key="i"
          :d="`M ${710 + i * 13} -36 C ${494 + i * 13} ${165 - i * 3}, ${1030 - i * 9} ${182 + i * 9}, ${784 + i * 19} 590`"
          stroke="currentColor" stroke-width=".7" />
      </svg>
    </div>
    <header v-if="kicker" class="atmos-kicker">
      <span aria-hidden="true" />
      {{ kicker }}
    </header>
    <main class="atmos-body"><slot /></main>
    <footer class="atmos-footer" aria-hidden="true">
      <span class="atmos-footer-line" />
      <span>{{ role === 'closing' ? 'END' : 'FIELD NOTES' }}</span>
    </footer>
  </div>
</template>
