<script setup>
import { ref } from 'vue';

const user = ref({
  name: '',
  age: null,
  subscribe: false,
  gender: 'male',
  interests: []
})

const submitForm = () => {
  console.log('Данные', user.value);
}
</script>

<template>
  <form @submit.prevent='submitForm'>
    <input v-model.trim='user.name' placeholder='Имя'>

    <input v-model.number='user.age' type='number' placeholder='Возраст'>
    <div>
      <label>
        <input type="radio" v-model='user.gender' value='male'>
        Мужской
      </label>
      <label>
        <input type="radio" v-model='user.gender' value='female'>
        Женский
      </label>
    </div>

    <select v-model='user.interests' multiple>
      <option value="sports">Спорт</option>
      <option value="music">Музыка</option>
    </select>
    <button type='submit'>Отправить</button>
  </form>
</template>
