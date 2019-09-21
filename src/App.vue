<template>
  <section id="app" class="container">
    <h1>Main App</h1>
    <Todos v-bind:todos="todo_data"/>
    
  </section>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todo_data: []
    }
  },
  mounted () {
    this.todo_data = [{"task":"aksujdhaskuf"}]
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  padding: 0 5rem;
}
</style>
