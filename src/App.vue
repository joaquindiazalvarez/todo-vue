<template>
  <input type="text"/>
  <ul id="todo">
    <li v-for="(element, index) in arr" v-bind:key="index">{{ element }}</li>
  </ul>
</template>

<script>

let arr = ['hola','chao'];
export default {
  name: 'App',
  components: {
  },
  data(){
    return{
    arr:arr
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
