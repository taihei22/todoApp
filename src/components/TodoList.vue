<template>
  <div>
    <button v-on:click="addTodo">ADD</button>
    <h5>Todo List</h5>
    <ul>
      <li v-for="(todo, i) in todos" v-bind:key="i">
        {{ todo }}
      <button v-on:click="deleteTodo(i)">DELETE</button>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    data(){
        return{
            todos: []
        }
    },
    created(){
        this.todos = JSON.parse(localStorage.getItem('todos')) || [];
    },
    methods: {
      deleteTodo(i){
        this.todos.splice(i, 1);
        localStorage.setItem('todos', JSON.stringify(this.todos));
      },
      addTodo(){
          this.$router.push('/todos/add');
      }
    }
  }
</script>