<template>
  <div>
    <button @click="decrement">-</button>
    <span>{{ count }}</span>
    <button @click="increment">+</button>
  </div>
</template>

<script setup>
import { ref, defineProps, defineEmits } from 'vue';

const props = defineProps({
  initialValue: { type: Number, default: 0 }
});

const emit = defineEmits(['change']);

const count = ref(props.initialValue);

const increment = () => {
  count.value++;
  emit('change', count.value);
};

const decrement = () => {
  count.value--;
  emit('change', count.value);
};
</script>