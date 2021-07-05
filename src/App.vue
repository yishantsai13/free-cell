<template>
  <div id="app">
    <layout></layout>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Layout from './components/Layout.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    Layout
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2A4254;
  /* margin-top: 60px; */
  background-color: #2A4254;
}
</style>
