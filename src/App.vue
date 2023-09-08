<script setup lang="ts">
import { ref } from 'vue'

const todos = ref<string[]>([])
const newTodo = ref<string>('')
const addTodo = () => {
  todos.value.push(newTodo.value)
  newTodo.value = ''
}
</script>

<template>
  <div class="flex flex-col items-center justify-center gap-2 min-h-screen">
    <div class="flex gap-2">
      <input type="text" v-model="newTodo" class="border" size="30" />
      <button @click="addTodo()" class="px-2 bg-gray-300 text-white">追加</button>
    </div>

    <ul>
      <li v-for="(todo, i) in todos" :key="i">{{ i }}. {{ todo }}</li>
    </ul>
  </div>
</template>
