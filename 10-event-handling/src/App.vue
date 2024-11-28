<script setup>
import { ref } from 'vue';

const greet = () => {

    alert(`xin chào`)
}

const sayHi = () => {
    alert(`say hi`)
}
const submit = () => {
    alert("submit form")
}

const key = () => {
    alert("hello")
}
</script>

<template>

    <button @click.self="greet">
        <span @click.self="sayHi">Say Hi</span>
        xin chào
    </button>

    <form @submit.prevent="submit">
        <button type="submit">submit</button>
    </form>

    <hr>
    <input @keyup.enter.alt="key" placeholder="nhập tại đây">
    <button @click.shift="key">click</button>
</template>
