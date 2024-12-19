<template>
  <div id="app">
    <h1 :style="{ color: headingColor }">{{ heading }}</h1>
    <MyComponent :prop1="value" />

    <div class="controls">
      <input v-model="value" placeholder="Type something..." />
      <button @click="resetValue">Reset</button>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue';
import MyComponent from './components/MyComponent.vue';

const value = ref('Hello from prop1.');
const headingColor = computed(() => (value.value.length > 15 ? 'red' : 'blue'));
const heading = computed(() => `Welcome to My Vue App with swarmakit: ${value.value}`);

const resetValue = () => {
  value.value = 'Hello from prop1.';
};

onMounted(() => {
  console.log('App is mounted!');
});
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.controls {
  margin-top: 20px;
}

input {
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-right: 10px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  color: white;
  background-color: #42b983;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #2a7a5b;
}
</style>
