<script setup>
import { computed, ref } from 'vue';


const isActive = ref(true)
const hasError = ref(false)

const classObject = computed(() => ({
    active: isActive.value && !hasError.value,
    hasError: hasError.value
}))

const changActive = () => {
    isActive.value = !isActive.value
}
</script>

<template>


    <button @click="changActive" class="button" :class="classObject">{{ isActive ? 'Active' : 'DeActive' }}</button>

    <button @click="changActive" class="button" :class="[isActive ? 'active' : '']">{{ isActive ? 'Active' : 'DeActive'
        }}</button>

</template>

<style>
.active {
    border: none;
    background: red;
    color: #fff;
    padding: 10px 14px;
    border-radius: 6px;
    cursor: pointer;

    &:hover {
        background-color: blue
    }
}
</style>
