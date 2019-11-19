<template>
  <div id="app">
    <!-- {{msg}} -->
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Todos v-bind:todos="todos" />
  </div>
</template>

<script>

import Todos from  './components/Todos.vue';

export default {
  name: 'app',
  components: {
        Todos
  },
  data(){
    return {
      // msg:'hello'
      todos:[
        {
          id:1,
          title:"Todo One",
          completed: true  
        },
        {
          id:2,
          title:"Todo two",
          completed: false  
        },
         {
          id:3,
          title:"Todo three",
          completed: true  
        }
      ]
    }
  }
}
</script>

<style>


* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
 