<template>
  <div class='elements'>
    <h2 :style='{ color: red }'>Реактивность</h2>
    <input v-model='form.name' placeholder='Имя'>
    <input v-model.number='form.age' type='number' placeholder='Возраст'>
    <button @click='submit'>отправить</button>
  </div>
  <div>
    <input v-model.number="form2.age" type="number" placeholder="Возраст" min="0" max="120">
    <p>Тип значения: {{ typeof form2.age }}</p>
    <p>Введённый возраст: {{ form2.age }}</p>
  </div>
</template>
<script setup>
import { ref, reactive } from 'vue'

const form2 = reactive({
  age: null // Начальное значение
});

const form = ref({
  name: '',
  age: null,
  hobbies: []
})

function submit() {
  console.log('отправлено:', form.value);
}
</script>

<style scope>
.elements {
  margin-bottom: 50px;
}
</style>