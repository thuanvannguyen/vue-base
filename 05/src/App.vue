<script setup>
import { ref } from 'vue'

const isLogin = ref(true)

const tooggleLogin = () => {
  isLogin.value = !isLogin.value
}

const userStatus = ref('online')

const changeStatus = () => {
  if (userStatus.value === 'online') {
    userStatus.value = 'away'
  } else if (userStatus.value === 'away') {
    userStatus.value = 'busy'
  } else if (userStatus.value === 'busy') {
    userStatus.value = 'online'
  }
}
// console.log(userStatus.value)

const isVisible = ref(true)

const toogleShow = () => {
  isVisible.value = !isVisible.value
}
</script>

<template>
  <h1 v-if="isLogin">Chào mừng người dùng đã đăng nhập!</h1>
  <h1 v-else>Chào mừng khách!</h1>
  <button @click="tooggleLogin">{{ isLogin ? 'Đăng xuất' : 'Đăng nhập' }}</button>
  <br />
  <h1 v-if="userStatus === 'online'">Người dung online</h1>
  <h1 v-else-if="userStatus === 'away'">Người dung đang vắng mặt</h1>
  <h1 v-else-if="userStatus === 'busy'">Người dung đang bận</h1>
  <h1 v-else>Người dung không rõ trạng thái</h1>

  <button @click="changeStatus">Thay đổi trang thái</button>
  <br />
  <h1 v-show="isVisible">Nội dung này ẩn hoặc hiển thị</h1>
  <button @click="toogleShow">{{ isVisible ? 'Ẩn' : 'Hiện' }}</button>
</template>

<style scoped>
</style>
