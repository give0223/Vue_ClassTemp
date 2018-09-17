<script>
import TodoInput from './TodoInput.vue'
import TodoItem from './TodoItem.vue'
 export default{
   data(){
     return {
       todos:[],
     }
   },
   methods:{
     addTodo(text){
       this.todos.push(text);
     },
     removeTodo(idx){
       this.todos.splice(idx,1);
     }
   },
   components:{
     TodoInput,
     TodoItem,
   },
 }; 
</script>

<template>
  <div>
    <TodoInput @submit="addTodo"/>
    <ul>
      <TodoItem 
        v-for=" (todo,idx) in todos" 
        :data="todo"
        @click.native="removeTodo(idx)"
      />
    </ul>
  </div>
</template>