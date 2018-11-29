<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Date :date="new Date()"/>
  </div>
</template>

<script>
import Date from "./components/Date.vue";

export default {
  name: "app",
  components: {
    Date
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
