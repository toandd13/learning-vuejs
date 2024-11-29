<script setup>
import { reactive, ref, watch } from 'vue';
const x = ref(0)
const y = ref(0)

const user = reactive({
    age: 19
})

watch(() => x.value + y.value, (sum) => {
    // console.log(`tổng của x và y là :${sum}`)
})


watch([x, () => y.value + 1], ([newX, newY]) => {
    console.log(`giá trị cập nhật là :${newX}, ${newY} `)
})

watch(user.age, (newAge) => {
    console.log(newAge)
})

const changeAge = () => {
    user.age = 20;
}


const increment = () => {
    x.value++
    y.value++
}
</script>


<template>

    <div>Watcher</div>
    {{ sum }}
    <button @click="increment">+</button>
    <br>
    {{ user.age }}
    <button @click="changeAge">Change Age</button>

</template>
