<script setup>
const sayHi1 = () => {
  alert(`Xin chào 1`);
};
const sayHi2 = () => {
  alert(`Xin chào 2`);
};
const submit = () => {
  alert("Form submitted");
};
</script>

<template>
  <h1>Event Handling</h1>
  <button @click="sayHi2">
    <button @click.stop="sayHi1">Chào 1</button>
    say hi 2
  </button>

  <form @submit.prevent="submit">
    <button type="submit">Submit</button>
  </form>
</template>


<!-- .stop ngăn chặn sự kiện pt con lên pt -->
<!-- .prevent ngăn chặn sự kiện load lai cua trinh duyet -->