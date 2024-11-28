<script setup>
import { ref } from 'vue';

const students = ref([
    {
        name: 'student A',
        age: 12,
        isActive: true
    },
    {
        name: 'student B',
        age: 13,
        isActive: true
    },
    {
        name: 'student C',
        age: 11,
        isActive: true
    }
])
</script>

<template>
    <div>
        <ul>
            <template v-for="(user, index) in students">
                <li v-if="user.isActive" :key="user.name">
                    {{ user.name }} : {{ user.isActive ? "Avtive" : "DeActive" }}({{ index }})
                </li>
            </template>
        </ul>
    </div>

    <span v-for="n in 10" :key="n">{{ n }}</span>
</template>
