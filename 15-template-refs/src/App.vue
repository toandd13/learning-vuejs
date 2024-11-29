<script setup>
import { onMounted, ref } from 'vue';

const inputRef = ref(null)
onMounted(() => {
    inputRef.value.focus();
})
</script>


<template>

    <div>Template refs</div>
    <input ref="inputRef">

</template>
