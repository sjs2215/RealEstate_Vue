<template>
<div id="app">
      <img alt="Vue logo" src="./assets/logo.png">

  <div class="container">
      <div class="row">

        <div class="col-md-2">
          <li v-on:click="sortPrice">가격순정렬</li>
          <li>글자순정렬</li>
          <li>원래대로</li>
        </div> 

        <div class="col-md-10">
          <div class="row">           
            <Card v-for="(별명, i) in Oneroom" v-bind:rooms="Oneroom[i]" v-bind:key="i"/>
          </div>
        </div>

      </div>  
  </div>
</div>
</template>

<script>
import Card from './components/Card.vue';
import Oneroom from './assets/rooms_post.js';

export default {
  name: 'App',
  components: {
    Card: Card,
  },
  data() {
    return {
      부모꺼: ['chicken', 'pizza', 'ramen', 'dumplings'],
      Oneroom: Oneroom,
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
