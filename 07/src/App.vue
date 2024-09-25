<script setup>
import { ref } from "vue";

const count = ref(0);
const greet = (event) => {
  console.log(event);
  alert(`Xin chao ${event.target.value}`);
};
</script>

<template>
  <div>
    <h1>{{ count }}</h1>
    <button @click="count++">Thêm 1</button>
    <br />
    <br />
    <button @click="greet">Chào</button>
  </div>
</template>