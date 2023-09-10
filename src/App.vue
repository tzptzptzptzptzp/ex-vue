<script setup lang="ts">
import { ref } from 'vue'
import AppHeader from './components/AppHeader.vue'
import TodoList from './components/TodoList.vue'

const todos = ref<string[]>([])
const newTodo = ref<string>('')

const addTodo = () => {
  todos.value.push(newTodo.value)
  newTodo.value = ''
}

const removeTodo = (i: number) => {
  todos.value.splice(i, 1)
}
</script>

<template>
  <div class="flex flex-col items-center justify-center gap-2 min-h-screen">
    <AppHeader color="pink">TodoList</AppHeader>
    <div class="flex gap-2">
      <input type="text" v-model="newTodo" class="border" size="30" />
      <button @click="addTodo()" class="px-2 bg-gray-300 text-white">追加</button>
    </div>

    <TodoList :todos="todos" @removeTodo="removeTodo" />
  </div>
</template>
