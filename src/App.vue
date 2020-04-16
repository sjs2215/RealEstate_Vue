<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <h4 v-if="flag">Hello world, this is {{name}}.</h4>

    <button v-on:click="hideName"> 이름 숨기기</button>

    <Card/>

  </div>
</template>

<script>
import Oneroom from './assets/rooms_post.js';
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Card: Card,
  },
  data() {
    return {
      name: "sarah",
      Oneroom: Oneroom,
      fonts: "font-size:26px",
      flag: "true",
      food: ['chicken', 'pizza', 'ramen', 'dumplings'],
    };
  },
  methods:{
    sortPrice(){
      this.Oneroom.sort(function(a,b){
        return a.price-b.price
      });
    },
    hideName(){
      this.flag=false;
    }
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
