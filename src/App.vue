<script setup>
import { computed } from 'vue'
const answer = computed(() => {
  return 1 + 1
})
</script>

<template>
  <div class="flex">
    <p>1 + 1 = {{ answer }}</p>
  </div>
</template>
