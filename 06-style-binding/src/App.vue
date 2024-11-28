<script setup>
import { reactive, ref } from 'vue';

const color = ref('red')
const background = ref('green')
const fontSize = ref(30)

const styleObject = reactive({
    border: 'none',
    borderRadius: '6px'
})
</script>

<template>

    <button :style="[
        {
            color,
            background,
            fontSize: fontSize + 'px'
        },
        styleObject
    ]">
        Active</button>
</template>
