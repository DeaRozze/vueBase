<template>
  <div class="app">
    <h1 class="title">Vue.js Учебник</h1>

    <section class="chapter-section">
      <h2 class="chapter-title">Синтаксис шаблонов</h2>
      <Chapter1 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Основы реактивности</h2>
      <Chapter2 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Вычисляемые свойства</h2>
      <Chapter3 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Работа с классами и стилями</h2>
      <Chapter4 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Условная отрисовка</h2>
      <Chapter5 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Отрисовка списков</h2>
      <Chapter6 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Обработка событий</h2>
      <Chapter7 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Работа с формами</h2>
      <Chapter8 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Наблюдатели</h2>
      <Chapter9 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Ссылки на элементы шаблона</h2>
      <Chapter10 />
    </section>

    <section class="chapter-section">
      <h2 class="chapter-title">Основы компонентов</h2>
      <Chapter11 />
    </section>
  </div>
</template>

<script setup>

import Chapter1 from './components/chapters/Chapter1.vue';
import Chapter2 from './components/chapters/Chapter2.vue';
import Chapter3 from './components/chapters/Chapter3.vue';
import Chapter4 from './components/chapters/Chapter4.vue';
import Chapter5 from './components/chapters/Chapter5.vue';
import Chapter6 from './components/chapters/Chapter6.vue';
import Chapter7 from './components/chapters/Chapter7.vue';
import Chapter8 from './components/chapters/Chapter8.vue';
import Chapter9 from './components/chapters/Chapter9.vue';
import Chapter10 from './components/chapters/Chapter10.vue';
import Chapter11 from './components/chapters/Chapter11.vue';

</script>

<style scoped>
.app {
  max-width: 800px;
  margin: 0 auto;
  padding: 30px 20px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f9f9f9;
  color: #444;
  line-height: 1.6;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}

.title {
  text-align: center;
  font-size: 36px;
  margin-bottom: 30px;
  color: #2c3e50;
}

.chapter-section {
  margin-bottom: 40px;
  padding: 20px;
  background-color: #fff;
  border-left: 5px solid #42b983;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

.chapter-title {
  font-weight: 600;
  margin-bottom: 15px;
}
</style>