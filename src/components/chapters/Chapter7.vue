<template>
  <button @click="increment">Счёт: {{ count }}</button>

  <div @mousemove="updateCoords" style="width: 300px; height: 200px; background: #eee; margin-top: 20px;">
    Координаты: {{ coords.x }}, {{ coords.y }}
  </div>

  <input @keyup.enter="console.log('Enter нажат!')" placeholder="Нажмите Enter">
</template>
<script setup>
import { ref } from 'vue';

const count = ref(0);
const coords = ref({ x: 0, y: 0 });

const increment = () => count.value++;
const updateCoords = (event) => {
  coords.value = { x: event.clientX, y: event.clientY };
};
</script>