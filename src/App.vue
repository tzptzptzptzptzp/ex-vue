<script setup lang="ts">
import { ref, computed } from 'vue'
const message = computed(() => {
  return 'ようこそ <strong>' + myName.value + '</strong>さん！'
})
const myColor = 'red'
const myName = ref('')
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">
    <div class="flex flex-col items-center gap-4">
      <div>
        <p>お名前は？： <input v-model="myName" type="text" class="px-1 border" /></p>
      </div>
      <p v-html="message" :style="{ color: myColor, fontSize: '2rem' }"></p>
    </div>
  </div>
</template>
