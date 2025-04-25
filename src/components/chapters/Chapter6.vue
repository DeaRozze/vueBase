<template>
  <!-- Для массивов: (item, index) -->
  <ul>
    <li v-for="(item, index) in items" :key="item.id">
      {{ index + 1 }}. {{ item.name }}
    </li>
  </ul>

  <!-- Для объектов: (value, key, index) -->
  <ul>
    <li v-for="(value, key, index) in user" :key="key">
      {{ index }}. {{ key }}: {{ value }}
    </li>
  </ul>
</template>

<script setup>
import { ref } from 'vue';

const items = ref([
  { id: 1, name: 'Яблоко' },
  { id: 2, name: 'Банан' }
]);

const user = ref({
  name: 'Анна',
  age: 25,
  city: 'Москва'
});</script>