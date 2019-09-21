<template>
  <section id="app" class="container">
    <h1 class="main-title">The Main App Component</h1>
    <Todos v-bind:todos="todos"/>
    
  </section>
</template>

<script>

import Todos from './components/Todos.vue';
import axios from 'axios';

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todos: []
    }
  },
  mounted () {
    axios.get('https://jsonplaceholder.typicode.com/todos')
    .then(response => {
      console.log(response.data)
      this.todos = response.data
    })
    .catch(error => console.log(error))
  }
}
</script>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.main-title {
  text-align: center;
  font-size: 2.8rem;
}

.container {
  padding: 0 5rem;
}
</style>
