<template>
  <div id="app">
    <Parent>
      <!-- Ini adalah konten yang akan disisipkan ke dalam slot di Parent -->
      <p>This is some content passed to the slot!</p>
    </Parent>
  </div>
</template>

<script>
import Parent from './components/parent.vue';

export default {
  name: 'App',
  components: {
    Parent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
