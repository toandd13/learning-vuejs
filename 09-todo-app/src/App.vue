<script setup>
import { reactive, ref } from 'vue';
const newTodo = ref("")
const todos = reactive([
    {
        id: 1,
        text: 'Leaning vuejs'
    },
    {
        id: 2,
        text: 'Leaning todo app'
    }

])
const addTodoNew = () => {
    if (newTodo.value.trim === "") return;
    const todo = {
        id: todos.length + 1,
        text: newTodo.value,
    }
    todos.push(todo)
    newTodo.value = "";
}
</script>

<template>
    <div>
        <input type="text" v-model="newTodo" @keyup.enter="addTodoNew">
        <button @click="addTodoNew">Add todo</button>
        <ul>
            <li v-for="item in todos" :key="item.id">
                {{ item.text }}
            </li>
        </ul>
    </div>
</template>
