<template>
  <div id="app">
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
  flex-direction: row;
  justify-content: center;
}

.todos {
  display: flex;
  width: 80%;
  flex-direction: column;
  background: #fafafa;
  border: 1px solid #e6e6e6;
  border-radius: 5px;
  padding: 20px;
}

.todo-item {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #e6e6e6;
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

.toggle {
  border: 1px solid #e6e6e6;
  padding: 2px;
  background-color: white;
}
</style>
