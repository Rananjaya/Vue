<template>
    <div>
         <!-- <h1>Todos Comp</h1> -->
         <div v-bind:key="todo.id" v-for="todo in todos">
            <!-- <h3>{{todo.title}}</h3> -->
            <TodoItem v-bind:todo="todo"/>
         </div>
        </div>
</template>
<script>

import TodoItem from './TodoItem';

export default {
    name:"Todos",
    components:{
       TodoItem
    },
    props: ["todos"],
  
}
</script>
<style scoped>

</style>