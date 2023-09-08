<script setup lang="ts">
import { ref } from 'vue'

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
    <div class="flex gap-2">
      <input type="text" v-model="newTodo" class="border" size="30" />
      <button @click="addTodo()" class="px-2 bg-gray-300 text-white">追加</button>
    </div>

    <ul>
      <li v-for="(todo, i) in todos" :key="i" class="flex items-center gap-2">
        {{ todo }}
        <span @click="removeTodo(i)" class="cursor-pointer">
          <svg xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 512 512">
            <path
              d="M256 48a208 208 0 1 1 0 416 208 208 0 1 1 0-416zm0 464A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM175 175c-9.4 9.4-9.4 24.6 0 33.9l47 47-47 47c-9.4 9.4-9.4 24.6 0 33.9s24.6 9.4 33.9 0l47-47 47 47c9.4 9.4 24.6 9.4 33.9 0s9.4-24.6 0-33.9l-47-47 47-47c9.4-9.4 9.4-24.6 0-33.9s-24.6-9.4-33.9 0l-47 47-47-47c-9.4-9.4-24.6-9.4-33.9 0z"
            />
          </svg>
        </span>
      </li>
    </ul>
  </div>
</template>
