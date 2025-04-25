<template>
  <form v-if="isLoginForm">
    <input type="email" placeholder="Email">
    <input type="password" placeholder="Пароль">
  </form>
  <form v-else>
    <input type="text" placeholder="Имя">
    <input type="email" placeholder="Email">
    <input type="password" placeholder="Пароль">
  </form>

  <button @click="isLoginForm = !isLoginForm">
    {{ isLoginForm ? 'Нет аккаунта? Зарегистрироваться' : 'Уже есть аккаунт? Войти' }}
  </button>

</template>
<script setup>
import { ref } from 'vue'
const isLoginForm = ref(true);
</script>