<template>
  <input class="task-input" type="text" v-model="task">
  <button @click="sayHi">Agregar tarea</button>
</template>

<script>
export default {
  data () {
    return {
      task: ''
    };
  },
  methods: {
    sayHi () {
      this.$emit('save', this.task);
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