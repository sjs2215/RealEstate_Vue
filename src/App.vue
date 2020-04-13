<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <h4>Hello world, this is {{name}}.</h4>

    <Card/>

  </div>
</template>

<script>
import Card from './components/Card.vue';
import Oneroom from './assets/rooms_post.js';

export default {
  name: 'App',
  components: {
    Card,
  },
  data() {
    return {
      name: "sarah",
      Oneroom: Oneroom,
    };
  },
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
