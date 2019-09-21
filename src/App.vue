<template>
  <section id="app">
    <section class="container">
      <h1>Main</h1>
    </section>
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
      todo_data: [
        { task: 'Laundry', by: 'Jeremy'} , 
        { task: 'Eating', by: 'Daniel'},
        { task: 'Exercise', by: 'Hannah'}
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  padding: 0 3rem;
}
</style>
