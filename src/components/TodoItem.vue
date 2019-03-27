<template>
    <div v-bind:class="['todo-item', todo.completed ? 'completed' : '']">
        <input
            type="checkbox"
            class="toggle"
            v-model="todo.completed">
        <p class="todo-item-text"> {{ todo.text }}</p>
        <button class="todo-item-delete" v-on:click="deleteTodo">X</button>
    </div>
</template>

<script>
export default {
    name: 'todoItem',
    props: ['todo'],
    methods: {
        deleteTodo() {
            this.$emit('delete', this.todo.id)
        }
    }
}
</script>

<style>

</style>
