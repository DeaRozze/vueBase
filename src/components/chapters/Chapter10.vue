<template>
  <input ref="inputRef" placeholder="Нажмите кнопку">
  <button @click="focusInput">Установить фокус</button>
</template>

<script setup>
import { ref } from 'vue';

const inputRef = ref(null);

const focusInput = () => {
  inputRef.value.focus();
};
</script>