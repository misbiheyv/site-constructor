<script setup lang="ts">
import { ref } from "@vue/reactivity";

const counter = ref(0);

function decrement() {
  counter.value--;
}

function increment() {
  counter.value++;
}
</script>

<template>
  <div class="container">
    <div class="counter__container">
      <button @click="decrement">уменьшить</button>
      <div>{{ counter }}</div>
      <button @click="increment">увеличить</button>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
}

.counter__container {
  display: flex;
  align-items: center;
  gap: 24px;
}

.counter__container > button {
  padding: 10px 20px;
  border: solid 1px rgb(46, 46, 46);
  border-radius: 3px;
  background: white;
}
</style>
