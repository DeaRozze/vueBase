<script setup>
import { ref, watch } from 'vue';

// 1. Создаем реактивные переменные
const name = ref('')
const message = ref('')

// 2. Наблюдаем за изменением name
watch(name, (newValue, oldValue) => {
  console.log('Старое имя:', oldValue)
  console.log('Новое имя:', newValue)

  if (newValue.length > 0) {
    message.value = `Привет, ${newValue}!`
  } else {
    message.value = 'Введите имя'
  }
})
</script>

<template>
  <div>
    <h1>Учим Watchers в Vue!</h1>

    <input v-model="name" placeholder="Введите ваше имя">

    <p v-if="message">{{ message }}</p>
  </div>
</template>

<style>
input {
  padding: 8px;
  font-size: 16px;
}

p {
  color: green;
  font-size: 18px;
}
</style>