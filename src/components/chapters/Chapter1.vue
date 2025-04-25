<template>
  <div>
    <h3>{{ title }}</h3>
    <input v-model="inputText" @keyup.enter="addItem">
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
        <button @click="removeItem(index)">×</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const title = 'Список дел'
const inputText = ref('')
const items = ref([])

const addItem = () => {
  if (inputText.value.trim) {
    items.value.push(inputText.value)
    inputText.value = ''
  }
}
const removeItem = (index) => {
  items.value.splice(index, 1)
}
</script>