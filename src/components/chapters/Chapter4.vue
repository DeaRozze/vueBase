<template>
  <div :style="{ color: activeColor, fontSize: fontSize + 'px' }">jjjj</div>
  <div>
    <button @click="isActive = !isActive" :class="{ 'active': isActive }">
      Кнопка
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const activeColor = ref('blue');
const fontSize = ref(16);

const isActive = ref(false);
</script>

<style>
.active {
  background: rgb(128, 0, 107);
}
</style>