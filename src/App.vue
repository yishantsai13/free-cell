<template>
  <div id="app">
    <layout></layout>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Layout from "./components/Layout.vue";

export default {
  name: "App",
  components: {
    // HelloWorld
    Layout,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $test-color;
  /* margin-top: 60px; */
  background-color: #2a4254;
}
body {
  margin: 0px;
}
* {
  box-sizing: border-box;
}
</style>
