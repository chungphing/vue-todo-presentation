<template>
    <div class="add-todo">
        <input type="text" class="add-todo-input" v-model="text">
        <button class="add-todo" v-on:click="addTodo">Add</button>
    </div>
</template>

<script>
export default {
    name: 'addTodo',
    data() {
        return {
            text: ''
        }
    },
    methods: {
        addTodo(text) {
            this.$emit('add', text)
        }
    }
}
</script>

<style>

</style>
