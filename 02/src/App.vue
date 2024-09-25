<script setup>
import { ref } from 'vue'

const count = ref('hello 500 anh em!')
console.log(count.value)

// Tuong tac qua phan value
</script>

<template>
  <h1>{{ count }}</h1>

  <!-- Doi voi template khong can value -->
</template>

<style scoped></style>
