<template>
    <AlertError :show="showError" message="a sua meta esta vazia" />
    <form class="form-todo-list">
        <input class="input-todo" type="text" v-model="todo" placeholder="o que precisa ser feito?"
            @keyup.enter="addtodo(todo)">
        <button class="btn" @click.prevent="addtodo(todo)">Add</button>
    </form>
</template>

<script setup lang="ts">

import { useStore } from '@/stores/todo';
import { ref } from 'vue';
import AlertError from './AlertError.vue';

const store = useStore()

const todo = ref<string>('')
const showError = ref<boolean>(false)

const addtodo = (item: string) => {
    const preventspace = item.trim()
    if (preventspace.length === 0) {
        showError.value = true
        setTimeout(() => {
            showError.value = false
        }, 3000);
        return
    }
    store.addTodo(preventspace)
    todo.value = ''
    showError.value = false
}

</script>

<style scoped>
.form-todo-list {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px 0;
}

.input-todo,
.btn {
    height: 40px;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 0 10px;
    margin-right: 10px;
}
</style>