<template>
    <div class="todos">
        <div class="todos-wrapper" v-if="todos.length > 0">
            <todo-item
            v-for="todo in todos"
            v-bind:key="todo.id"
            v-bind:todo="todo"
            v-on:delete="deleteTodo"
            />
        </div>
        <div v-else>
            <h2>It's look empty in here, try adding a note</h2>
        </div>
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
          this.todos = this.todos.filter(todo => todo.id !== id)
      },
      addTodo(text){
        //add todo here
        this.todos = [...this.todos, {
            id: this.todos.length+1,
            text: text,
            completed: false
        }]
      }
  }
}
</script>

<style>

</style>
