<script setup>
const message = 'Toi ten Nguyen Van Thuan'
const rawHtml = '<span style="color: red">This should be red.</span>'
const buttonId = 'button-id'
const buttonName = 'button-id-name'
const buttonClass = 'btn btn-rounded'
const isButtonDisabled = true
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: {
    color: 'blue'
  }
}
const number = 1
const lisString = 'a,b,c,d,e,f,j'
</script>

<template>
  <h1>Hello 500 anh em!</h1>

  <!-- 1. Noi suy van ban: -->
  <h2>Message: {{ message }}</h2>

  <!-- 2. HTML Tho -->
  <p>Render HTML BTH: {{ rawHtml }}</p>
  <p v-html="rawHtml"></p>

  <!-- 3.1 Rang buoc thuoc tinh -->
  <button v-bind:id="buttonId">Click here!</button>

  <!-- 3.2 Rang buoc thuoc tinh - bi danh -->
  <button :id="buttonName" :class="buttonClass">Click here!</button>

  <!-- 4. Thuộc Tính Boolean -->
  <button :disabled="isButtonDisabled">{{ isButtonDisabled ? 'disabled' : 'click here' }}</button>

  <!-- 5. Rang buoc nhieu thuoc tinh -->
  <button v-bind="objectOfAttrs">click here!!!!</button>

  <!-- 6. 
  Su dung bieu thuc trong Binding (Rang buoc)
   -->
  <button :id="lisString.split(',').join('-')">Number: {{ number * 2 }}</button>
</template>
