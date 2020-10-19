<template>
  <div id="app">
    <Main />
    <Universe />
  </div>
</template>

<script>
import Main from './components/Main.vue'
import Universe from './components/Universe.vue';
export default {
  name: 'App',
  components: {
    Main,
    Universe
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
