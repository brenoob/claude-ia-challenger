<template>
    <div class="todo-list">
        TodoList
        <div  :class="{'completed': todo.completed}" class="list" v-for="todo in todoList" :key="todo.id">
            <span>
                {{ todo.item }}
            </span>
            <div>
                <template v-if="!todo.completed">
                    <span @click="toggleCompleted(todo.id)">
                        <ConfirmCircle />
                    </span>
                </template>
                <span @click="deleteTodo(todo.id)">
                    <TrashCircle />
                </span>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { useStore } from '@/stores/todo';
import { storeToRefs } from 'pinia';
import TrashCircle from './icons/TrashCircle.vue';
import ConfirmCircle from './icons/ConfirmCircle.vue';

const store = useStore();
const { todoList } = storeToRefs(store);
const { toggleCompleted, deleteTodo} = store

</script>

<style scoped>
.todo-list {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
}
.list {
    margin: 0.5rem;
    display: flex;
    justify-content: space-between;
    padding: 0 1rem;
    font-size: 1.5rem;
}
.completed {
    background-color: hsla(160, 100%, 37%, 1);
    border-radius: 5px;
}
svg {
    cursor: pointer;
}
svg:hover {
    opacity: 0.8;
}
</style>