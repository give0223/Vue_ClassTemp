<template>
  <li class="todo-item">
    {{data}}
  </li>
</template>

<script>
  export default{
    props:['data'],
  }
</script>

<style>
  .todo-item{
    font-size: 1.2em;
    background-color: #def;
    margin: 5px;
  }
</style>