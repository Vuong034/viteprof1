<script setup>
defineProps({
  todos: Array,
});
</script>

<template>
  <ul>
    <li v-for="todo in todos">
      {{ todo }}
    </li>
  </ul>
</template>

<style scoped></style>
