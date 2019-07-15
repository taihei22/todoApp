<template>
  <div>
    <h3>My Todo</h3>
    <router-view></router-view>
    <!-- <todo-form v-on:add="addTodo($event)"></todo-form>
    <todo-list v-bind:todos="todos" v-on:delete="deleteTodo($event)"></todo-list> -->
    <!-- <todo-form></todo-form>
    <todo-list></todo-list> -->
  </div>
</template>

<script>
import TodoForm from './components/TodoForm'
import TodoList from './components/TodoList'

  export default {
    // data(){
    //   return{
    //     todos: []
    //   }
    // },
    // created(){
    //   this.todos = JSON.parse(localStorage.getItem('todos')) || [];
    // },
    components: {
      'todo-form': TodoForm,
      'todo-list': TodoList
    },
    // methods: {
    //   addTodo(newTodo){
    //     this.todos.push(newTodo);
    //     localStorage.setItem('todos', JSON.stringify(this.todos));
    //   },
    //   deleteTodo(i){
    //     this.todos.splice(i, 1);
    //     localStorage.setItem('todos', JSON.stringify(this.todos));
    //   }
    // }
  }
</script>