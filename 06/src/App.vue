<script setup>
import { ref } from "vue";

// Array
const shoppingItem = ref([
  {
    name: "apple",
    price: 7,
  },
  {
    name: "orange",
    price: 12,
  },
]);

// 
</script>

<template>
  <div>
    <ul>
      <li v-for="item in shoppingItem" :key="item.name">
        {{ item.name }}
      </li>
    </ul>
    <span v-for="n in 10" :key="n">{{ n }}</span>
  </div>
</template>
