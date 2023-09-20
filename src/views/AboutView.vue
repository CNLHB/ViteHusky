<script setup>
import { useCounterStore } from '@/stores/counter';
const store = useCounterStore();
function handleClick() {
  console.log('x');
  store.increment();
}
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>{{ store.count }}$</h1>
    <h1><button @click="handleClick">add</button></h1>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
