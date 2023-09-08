<script setup lang="ts">
defineProps(['color'])
</script>

<template>
  <header>
    <h1 :style="{ color: color }" class="text-2xl"><slot>No Title</slot></h1>
  </header>
</template>
