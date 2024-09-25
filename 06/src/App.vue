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

// Object
const user = ref({
  firtName: "John",
  lastName: "Doe",
  age: 30,
});
const users = ref([
  {
    name: "John",
    age: 30,
    isActive: true,
  },
  {
    name: "Teo",
    age: 20,
    isActive: false,
  },
]);
</script>

<template>
  <div>
    <h1>Array</h1>
    <ul>
      <li v-for="item in shoppingItem" :key="item.name">
        {{ item.name }}
      </li>
    </ul>
    <span v-for="n in 10" :key="n">{{ n }}</span>
    <h1>Object</h1>
    <ul>
      <li v-for="(value, key, index) in user" :key="index">
        {{ value }} - {{ key }} - ({{ index }})
      </li>
    </ul>
    <ul>
      <template v-for="(user, index) in users">
        <li v-if="!user.isActive" :key="user.name">
          {{ user.name }} : {{ user.isActive ? "active" : "no-active" }} - ({{
            index
          }})
        </li>
      </template>
    </ul>
  </div>
</template>
