<template>
  <div class="about">
    <h1>Timer:{{ time }}</h1>
  </div>
</template>


<script setup>
import { onBeforeMount, onBeforeUnmount, onMounted, onUnmounted, ref } from 'vue';

const time = ref(0)
let intervalId = null

onMounted(() => {
  console.log("onMounted")
  intervalId = setInterval(() => {
    time.value++
  }, 100)
})
onBeforeMount(() => {
  console.log("onBeforeMount")
})

onUnmounted(() => {
  console.log("onUnmounted")
  clearInterval(intervalId)
})

onBeforeUnmount(() => {
  console.log("onBeforeUnmount")
})
</script>
