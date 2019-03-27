<template>
    <div class="todos">
        <todo-item 
            v-for="todo in todos" 
            v-bind:key="todo.id" 
            v-bind:todo="todo"
            v-on:delete="deleteTodo"
            />
        <add-todo v-on:add="addTodo" />
    </div>
</template>

<script>
import TodoItem from './TodoItem'
import AddTodo from './AddTodo'

export default {
    name: 'todos',
    components: {
        TodoItem,
        AddTodo
    },
    data() {
        return {
            todos: [
                {
                id: 1,
                text: 'hello world!',
                completed: false,
                },
                {
                id: 2,
                text: 'hi there!',
                completed: false,
                },
                {
                id: 3,
                text: 'goodbye!',
                completed: false,
                },
            ]
        }
  },
  methods: {
      deleteTodo(id) {
          //delete todo here
          console.log(id);
      },
      addTodo(text){
          //add todo here
          console.log(text);
          
      }
  }
}
</script>

<style>

</style>
