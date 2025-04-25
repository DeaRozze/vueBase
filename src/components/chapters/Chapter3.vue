<template>
  <div> Первый пример: <p>Полное имя: {{ fullName }}</p>
  </div>

  <div>
    <input v-model="searchQuery" placeholder="Поиск...">
    <ul>
      <li v-for="product in filteredProducts" :key="product.name">
        {{ product.name }} - {{ product.price }} ₽
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const firstName = ref('Vlad');
const lastName = ref('Kudi');

const fullName = computed(() => `${firstName.value} ${lastName.value}`);

const searchQuery = ref('');
const products = ref([
  { name: 'Ноутбук', price: 1000 },
  { name: 'Телефон', price: 500 }
]);

// Фильтрация товаров
const filteredProducts = computed(() => {
  return products.value.filter(product =>
    product.name.toLowerCase().includes(searchQuery.value.toLowerCase())
  );
});
</script>
