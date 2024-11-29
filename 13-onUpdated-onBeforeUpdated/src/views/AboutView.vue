<template>
  <div class="about">
    <h1 id="count">Count: {{ count }}</h1>
    <button @click="increment">+</button>
  </div>
</template>


<script setup>
import { onBeforeUpdate, onUpdated, ref } from 'vue';

const count = ref(0)

const increment = () => {
  count.value++;
}

onUpdated(() => {
  console.log("on updated", document.getElementById("count").textContent)
})
onBeforeUpdate(() => {
  console.log("on before update", document.getElementById("count").textContent)
})
</script>
