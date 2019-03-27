<template>
    <div class="add-todo">
        <input type="text" class="add-todo-input" placeholder="Need to write down something? " v-model="text">
        <button class="add-todo-button" v-on:click="addTodo">Add</button>
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
        addTodo() {
            this.$emit('add', this.text)
            this.text = ''
        }
    }
}
</script>

<style>

</style>
