<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <h4>Hello world, this is {{name}}.</h4>
    <p v-bind:style="fonts">font size</p>

    <button v-on:click="sortPrice">가격순으로 정렬하기</button>

    <p>{{Oneroom[2].title}}</p>
    <img v-bind:src="Oneroom[2].image" alt="">
    <p>{{Oneroom[2].caption}}</p>
    <p>{{Oneroom[2].price}}</p>

    <p>{{Oneroom[1].title}}</p>
    <img v-bind:src="Oneroom[1].image" alt="">
    <p>{{Oneroom[1].caption}}</p>
    <p>{{Oneroom[1].price}}</p>

    <p>{{Oneroom[0].title}}</p>
    <img v-bind:src="Oneroom[0].image" alt="">
    <p>{{Oneroom[0].caption}}</p>
    <p>{{Oneroom[0].price}}</p>


  </div>
</template>

<script>
import Oneroom from './assets/rooms_post.js';

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      name: "sarah",
      Oneroom: Oneroom,
      fonts: "font-size:26px",
    };
  },
  methods:{
    sortPrice(){
      this.Oneroom.sort(function(a,b){
        return a.price-b.price
      });
    },
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
