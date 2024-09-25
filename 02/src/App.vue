<script setup>
import { nextTick, ref } from 'vue'

const count = ref(3)
console.log(count.value)

const object = ref({
  user: 'test',
  age: '30'
})

// script: Tuong tac qua phan value

// 2. nextTick()
const number = ref(0)

const handleIncrement = async () => {
  number.value++
  console.log(document.getElementById('count').innerText)
  await nextTick()
  console.log(document.getElementById('count').innerText)
}
</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="count++">Increment</button>

  <h1>{{ object.user }}</h1>

  <!-- // 2. nextTick() -->
  <h3 id="count">{{ number }}</h3>

  <button @click="handleIncrement">Incree</button>
</template>

<style scoped></style>

<!-- Template khong can value -->