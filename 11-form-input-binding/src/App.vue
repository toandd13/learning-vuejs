<script setup>
import { ref } from 'vue';

const text = ref('hello')

const multilineText = ref("");

const checkName = ref([])
const radio = ref('')
const select = ref('')

const checked = ref('')


const luaChon1 = ref('lựa chọn 1')
const luaChon2 = ref('lựa chọn 2')
</script>

<template>
    <div>
        <input v-model.lazy="text" />
        <p>text: {{ text }}</p>

        <textarea v-model="multilineText" placeholder="Input your message" />
        <p>Multiline Text: {{ multilineText }}</p>

        <hr>
        <p>check box:{{ checkName }}</p>
        <input type="checkbox" id="a" v-model="checkName" :value="luaChon1">
        <label for="a">A</label>
        <input type="checkbox" id="b" v-model="checkName" :value="luaChon2">
        <label for="b">B</label>
        <input type="checkbox" id="c" v-model="checkName" value="C">
        <label for="c">C</label>


        <p>checked:{{ checked }}</p>
        <input type="checkbox" id="a" v-model="checked" true-value="yes" false-value="no">




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
            <option value="Ây">A</option>
            <option value="Bi">B</option>
            <option value="Ci">C</option>

        </select>
    </div>
</template>
