<template>
  <div>
    <ul>
      <li v-for="이름들 in food" v-bind:key="이름들">{{이름들}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{

    };
  }
}
</script>

<style>

</style>