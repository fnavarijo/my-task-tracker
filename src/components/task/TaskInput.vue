<template>
  <input class="task-input" type="text">
  <button @click="sayHi">Agregar tarea</button>
</template>

<script>
export default {
  methods: {
    sayHi () {
      console.log('HI');
    }
  }
}
</script>

<style scoped>
.task-input {
  border-radius: 0.5rem;
  padding: 1rem 0.5rem;
}
</style>