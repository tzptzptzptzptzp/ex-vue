<script setup>
import { computed } from 'vue'
const answer = computed(() => {
  return 1 + 1
})
const message = 'ようこそ <strong>〇〇</strong>さん！'
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">
    <div>
      <p v-html="message"></p>
    </div>
  </div>
</template>
