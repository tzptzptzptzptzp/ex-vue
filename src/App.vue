<script setup lang="ts">
import { ref } from 'vue'
const number = ref(0)

const add = () => {
  number.value++
}
</script>

<template>
  <div class="flex items-center justify-center gap-2 min-h-screen">
    <input type="text" v-model="number" class="border" size="30" />
    <button @click="add" class="px-2 bg-gray-300 text-white">+1</button>
  </div>
</template>
