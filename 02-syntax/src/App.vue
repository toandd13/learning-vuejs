<script setup>
const message = "hello world"
const rawHtml = '<div><h1>title</h1><span style="color:red">This should be red.</span></div>'
const buttonId = 'button-id'
const classId = 'class-id'
const isButtonDisable = true
const number = 1
const listString = 'a.b.c.d.e.f.g,h,i'

const objectOfAttribute = {
  id: 'container',
  class: 'wrapper',
  style: {
    color: 'red'
  }
}

const convertToId = (data) => data.split(',').reverse().join('-')
const attributeName = 'href'
const url = 'http://ap.poly.edu.vn'
</script>

<template>
  <h1>Syntax</h1>
  message : {{ message }}
  <span v-html="rawHtml"></span>
  <button :id="buttonId" :class="classId" :disabled="isButtonDisable">{{ isButtonDisable ? 'Disabled' : 'click here' }}

  </button>
  <button v-bind="objectOfAttribute">Click here</button>
  <button :id="convertToId(listString)">number:{{ number * 2 }}</button>
  <a v-bind:[attributeName]="url">go to ap.poly.edu.vn</a>
</template>
