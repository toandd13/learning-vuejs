<script setup>

import { nextTick, ref } from 'vue'
const count = ref(0)

const increase = async () => {
    count.value++
    console.log(document.getElementById('count').innerText)
    await nextTick()
    console.log(document.getElementById('count').innerText)
}
</script>

<template>
    <p>count:{{ count }}</p>

    <button @click="increase">insert</button>
</template>
