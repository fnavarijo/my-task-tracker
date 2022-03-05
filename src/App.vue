<template>
  <article class="time-tracker">
    <AppHeader />
    <TaskInput @save="saveToList" />
    <TaskList :list="list" />
  </article>
</template>

<script setup>
import { ref } from 'vue';

import AppHeader from './components/AppHeader.vue'
import TaskInput from './components/task/TaskInput.vue';
import TaskList from './components/task/TaskList.vue'; 

const list = ref([]);

function saveToList (task) {
  list.value.push(task);
}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;600&display=swap');

html {
  background-color: white;
  font-family: 'Quicksand', sans-serif;
}

.time-tracker {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
