<script setup>
import { ref } from 'vue';

const login = ref(true)
const toggleLogin = () => {
    login.value = !login.value
}

const userStatus = ref("online")

const changeStatus = () => {
    if (userStatus.value === 'online') {
        userStatus.value = 'away'
    } else if (userStatus.value === 'away') {
        userStatus.value = 'busy'
    } else if (userStatus.value === 'busy') {
        userStatus.value = 'online'
    }
}

const showStatus = ref(true)

const changeShowStatus = () => {
    showStatus.value = !showStatus.value
}
</script>

<template>
    <h1 v-if="login">Chào mừng người dùng đã đăng nhập</h1>
    <h1 v-else>Chào mừng người dùng </h1>

    <button @click="toggleLogin">{{ login ? 'Đăng xuất' : 'Đăng nhập' }}</button>
    <hr />

    <h1 v-if="userStatus === 'online'">Nguời dùng đang online</h1>
    <h1 v-else-if="userStatus === 'away'">Nguời dùng đang away</h1>
    <h1 v-else-if="userStatus === 'busy'">Nguời dùng đang busy</h1>
    <h1 v-else>Nguời dùng đang không xác định</h1>
    <button @click="changeStatus">Thay đổi trạng thái</button>


    <hr />
    <h1 v-show="showStatus">Nội dung đang được hiển thị</h1>
    <button @click="changeShowStatus">{{ showStatus ? 'Ẩn' : 'Hiện' }}</button>
</template>
