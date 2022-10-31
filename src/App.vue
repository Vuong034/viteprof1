<script setup>
import List from './components/List.vue';
import { ref } from 'vue';

const todos = ref([]);
const newTodo = ref('');

function handleSubmit() {
  todos.value.push(newTodo);
  newTodo.value = '';
}
</script>

<template>
  <h1>Todo List</h1>
  <List :todos="todos" />
  <form @submit.prevent="handleSubmit">
    <input type="text" placeholder="Write a new task" v-model="newTodo" />
    <button type="submit">Add</button>
  </form>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
