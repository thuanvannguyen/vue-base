<script setup>
import { computed, ref } from "vue";

const firstName = ref("Nguyen Van");
const lastName = ref("A");

const fullName = computed({
  get() {
    return firstName.value + " " + lastName.value;
  },
  set(newValue) {
    [firstName.value, lastName.value] = newValue.split(",");
  },
});

const handleChangeName = () => {
  fullName.value = "Nguyen van, teo"
};
</script>

<template>
  <p>FullName: {{ fullName }}</p>
  <button @click="handleChangeName">Change Name</button>
</template>