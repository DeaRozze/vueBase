<template>
  <div class="app">
    <h1 class="title">Vue.js Учебник</h1>

    <section class="chapter-sections" v-for="chapter in chapters" :key="chapter.title">
      <h2 class="chapter-title">{{ chapter.title }}</h2>
      <component :is="chapter.component" />
    </section>
  </div>

  <input :value='text' @input="event => text = event.target.value">
  <p>v-model без v-model: {{ text }}</p>
  <ul>
    <li v-for="(item, index) in items" :key="item.id" :class="{ 'done-item': doneIndex.includes(index) || allDone }">
      {{ item }}
    </li>
  </ul>
</template>
<script setup>
import { ref } from 'vue';
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

const chapters = [
  { title: 'Синтаксис шаблонов', component: Chapter1 },
  { title: 'Основы реактивности', component: Chapter2 },
  { title: 'Вычисляемые свойства', component: Chapter3 },
  { title: 'Работа с классами и стилями', component: Chapter4 },
  { title: 'Условная отрисовка', component: Chapter5 },
  { title: 'Отрисовка списков', component: Chapter6 },
  { title: 'Обработка событий', component: Chapter7 },
  { title: 'Работа с формами', component: Chapter8 },
  { title: 'Наблюдатели', component: Chapter9 },
  { title: 'Ссылки на элементы шаблона', component: Chapter10 },
  { title: 'Основы компонентов ', component: Chapter11 },
]
const textSize = ref(20);
const doneIndex = ref([]);
const allDone = ref(false)
const items = ref([])
</script>
<style scoped>
/* v-bind в CSS */
.done-item {
  text-decoration: line-through;
  font-size: v-bind('textSize + "px"');
}

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

.chapter-sections {
  margin-bottom: 40px;
  padding: 20px;
  background-color: #fff;
  border-left: 5px solid #42b983;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

.chapter-title {
  color: #2c3e50;
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid #eee;
}
</style>