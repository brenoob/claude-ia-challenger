<template>
    <form class="form-todo-list">
        <input class="input-todo" type="text" v-model="todo" placeholder="What needs to be done?" @keyup.enter="addtodo(todo)">
        <button class="btn" @click.prevent="addtodo(todo)">Add</button>
    </form>
</template>

<script setup lang="ts">
import { useStore } from '@/stores/todo';
import { ref } from 'vue';

const store = useStore()

const todo = ref<string>('')

const addtodo = (item: string) => {
    if (item.length === 0) {
        return
    }
    store.addTodo(item)
    todo.value = ''
}

</script>

<style scoped>
.form-todo-list {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px 0;
}
.input-todo, .btn {
    height: 40px;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 0 10px;
    margin-right: 10px;
}
</style>