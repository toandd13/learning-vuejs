<script setup>
import { ref } from 'vue';

const text = ref('hello')

const multilineText = ref("");

const checkName = ref([])
const radio = ref('')
const select = ref('')
</script>

<template>
    <div>
        <input v-model="text" />
        <p>text: {{ text }}</p>

        <textarea v-model="multilineText" placeholder="Input your message" />
        <p>Multiline Text: {{ multilineText }}</p>

        <hr>
        <p>check box:{{ checkName }}</p>
        <input type="checkbox" id="a" v-model="checkName" value="A">
        <label for="a">A</label>
        <input type="checkbox" id="b" v-model="checkName" value="B">
        <label for="b">B</label>
        <input type="checkbox" id="c" v-model="checkName" value="C">
        <label for="c">C</label>

        <p>radio:{{ radio }}</p>
        <input type="radio" id="a" v-model="radio" value="A">
        <label for="a">A</label>
        <input type="radio" id="b" v-model="radio" value="B">
        <label for="b">B</label>
        <input type="radio" id="c" v-model="radio" value="C">
        <label for="c">C</label>

        <p>select:{{ select }}</p>
        <select v-model="select">
            <option disabled value="">Please select</option>
            <option>A</option>
            <option>B</option>
            <option>C</option>

        </select>
    </div>
</template>
