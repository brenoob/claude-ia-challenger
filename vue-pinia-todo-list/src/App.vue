<script setup lang="ts">
import AppTodoList from './components/AppTodoList.vue'
</script>

<template>
  <header>
    <h1 class="green"> Vue + <span class="pinia">Pinia</span> TodoList</h1>
  </header>

  <main>
    <AppTodoList />
  </main>
</template>

<style scoped>
header {
  display: flex;
  justify-content: center;
  margin: 55px 0;
  line-height: 1.5;
}

main {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
