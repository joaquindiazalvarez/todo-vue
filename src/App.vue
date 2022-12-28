<template>
  <h1>Inserte tarea</h1>
    <input type="text" v-model="task" v-on:keyup.enter="submitForm"/>
  <ul id="todo">
    <li v-for="(element, index) in arr" v-bind:key="index"><span>{{ element }}
      <svg @click="deleteItem(element)" xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-x" viewBox="0 0 16 16">
      <path d="M4.646 4.646a.5.5 0 0 1 .708 0L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 0 1 0-.708z"/>
</svg></span>
</li>
  </ul>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return{
    task:"",
    arr:[]
    }
  },
  methods: {
    deleteItem(element){
      this.arr.splice(this.arr.indexOf(element),1);
      console.log("hola")
    },
    submitForm(e){
      this.arr.push(this.task);
      this.task = ""
      e.preventDefault()
      console.log("hola")
    }
  }
}
  
</script>

<style src="./main.css">

</style>
