<script setup>

import { ref, computed } from 'vue'
const firstName = ref('Nguyễn Văn')
const lastName = ref('A')

const fullName = computed({
    get() {
        return firstName.value + ' ' + lastName.value
    },
    set(newValue) {
        [firstName.value, lastName.value] = newValue.split(',')
    }
})

const changeFullName = () => {

    fullName.value = "Nguyễn Thị, B"
}

</script>

<template>
    <p>FirstName:{{ firstName }}</p>
    <p>LastName:{{ lastName }}</p>
    <p>FullName:{{ fullName }}</p>

    <button @click="changeFullName">Change FullName</button>

</template>
