<script setup>
import { computed } from 'vue'
const answer = computed(() => {
  return 1 + 1
})
const message = 'ようこそ <strong>〇〇</strong>さん！'
const myColor = 'red'
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">
    <div>
      <p v-html="message" :style="{ color: myColor, fontSize: '2rem' }"></p>
    </div>
  </div>
</template>
