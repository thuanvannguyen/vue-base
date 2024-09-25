<script setup>
import { computed, nextTick, reactive, ref } from 'vue'

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

// Computed
const book = reactive({
  name: 'Book 1',
  chapters: []
})

const addChapter = () => {
  book.chapters.push('chapter')
}

const isPublished = computed(() => (book.chapters.length > 0 ? 'Có' : 'Không'))
</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="count++">Increment</button>

  <h1>{{ object.user }}</h1>

  <!-- // 2. nextTick() -->
  <h3 id="count">{{ number }}</h3>

  <button @click="handleIncrement">Incree</button>
  <br />
  <!-- // Computed -->

  <p>Book name: {{ book.name }}</p>
  <p>Đã xuất bản: {{ isPublished }}</p>
  <button @click="addChapter">Incree</button>
</template>

<style scoped></style>

<!-- Template khong can value -->