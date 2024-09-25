<script setup>
import { ref } from 'vue'

const count = ref(3)
console.log(count.value)

// script: Tuong tac qua phan value
</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="count++">Increment</button>

  <!-- Template khong can value -->
</template>

<style scoped></style>
