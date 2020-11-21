<template>

<!--@author Isac Canedo-->

  <div id="app">
    <div class="container">
      <AddTodo />
      <FilterTodos />
      <Todos />      
    </div>
  </div>
</template>

<script>
import Todos from './components/Todos.vue';
import AddTodo from './components/AddTodo.vue';
import FilterTodos from './components/FilterTodos.vue';

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo,
    FilterTodos
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

body {
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

.container {
  width: 80%;
  margin: 0 auto;
}
</style>
