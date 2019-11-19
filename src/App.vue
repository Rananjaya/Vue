<template>

  <div id="app">
    <Header/>
      <AddTodo/>
    <!-- {{msg}} -->
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Todos v-bind:todos="todos" v-on:del-todo="deleTodo"/>
  
  </div>
</template>

<script>

import Todos from  './components/Todos.vue';
import Header from './layout/Header.vue';
import AddTodo from './components/AddTodo.vue';

export default {
  name: 'app',
  components: {
        Todos,
        Header,
        AddTodo
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
  },
  methods:{
    deleTodo(id){

      this.todos = this.todos.filter(todo => todo.id !== id)

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
  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background: #666;
  }
</style>
 