
<template>
  <div id='app'>
  <h1>Welcome to My Vue App with swarmakit</h1>
<MyComponent :prop1="value"/>
  </div>
</template>

<script setup>
    import MyComponent from './components/MyComponent.vue'
    const value = 'Hello from prop1.';
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
</style>
