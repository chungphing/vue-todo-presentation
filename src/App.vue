<template>
  <div id="app">
    <h1>Vue Todo</h1>
    <todos />
  </div>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
  name: 'app',
  components: {
    Todos
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.todos {
  display: flex;
  width: 80%;
  flex-direction: column;
  background: #fafafa;
  border: 1px solid #e6e6e6;
  border-radius: 5px;
}

.todo-item {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #e6e6e6;
  padding: 8px;

}
.todo-item-delete {
  border: 1px solid #ff7474;
  border-radius: 5px;
  color: #ff7474;
  font-weight: bold;
  padding: 5px;
  background: rgba(0,0,0,0);
}
.todo-item-delete:hover {
  color: white;
  background: #b32323;
  cursor: pointer;
}
.completed {
  background-color: #e6e6e6;
}
.completed .todo-item-text {
  text-decoration: line-through;
}

.toggle {
  border: 1px solid #e6e6e6;
  padding: 2px;
  background-color: white;
}


.add-todo {
  margin: 20px 0 5px 0;
  padding: 8px;
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.add-todo-input {
  padding: 15px;
  width: 100%;
  margin: 0 5px;
  border-radius: 5px;
  border: 1px solid #e6e6e6;
}
.add-todo-button {
  cursor: pointer;
  border: 2px solid #e6e6e6;
  width: 100px;
  padding: 14px;
  border-radius: 5px;
  font-size: 10pt;
}
.add-todo-button:hover {
  color: white;
  background-color: #22e1bd;
  border-color: #23bc9f;
}



</style>
