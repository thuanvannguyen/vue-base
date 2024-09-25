<script setup>
import { ref } from "vue";

// binding qua doi tuong
const isAcitve = ref(false);
</script>

<template>
  <div>
    <button class="button" :class="{ active: isAcitve }">Active</button>
  </div>
</template>

<style scoped>
button {
  border: none;
  background: gray;
  color: #fff;
  padding: 5px 15px;
  border-radius: 3px;
  cursor: pointer;
}
.active {
  border: none;
  background: green;
  color: #fff;
  padding: 5px 15px;
  border-radius: 3px;
  cursor: pointer;
}
.error {
  border: none;
  background: red;
  color: #fff;
  padding: 5px 15px;
  border-radius: 3px;
  cursor: pointer;
}
</style>
