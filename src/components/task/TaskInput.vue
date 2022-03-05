<template>
  <input class="task-input" type="text" v-model="task">
  <button @click="saveTask">Agregar tarea</button>
</template>

<script setup>
import { ref, defineEmits } from 'vue';

const emit = defineEmits(['save'])

const task = ref('');

function saveTask() {
  emit('save', task.value)
}
</script>

<style scoped>
.task-input {
  border-radius: 0.5rem;
  padding: 1rem 0.5rem;
}
</style>