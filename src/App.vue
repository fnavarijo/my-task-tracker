<template>
  <article class="time-tracker">
    <AppHeader />
    <TaskInput />
    <TaskList :list="['Terminar codigo', 'hacer aquello']" />
  </article>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import TaskInput from './components/task/TaskInput.vue';
import TaskList from './components/task/TaskList.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    TaskInput,
    TaskList
  }
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
