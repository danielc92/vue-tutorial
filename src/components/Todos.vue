<template>
    <section>
       <div v-for="(todo, index) in todos" v-bind:key="index">
            <TodoItem v-bind:todo="todo"/>
        </div>
    </section>
</template>

<script>
import TodoItem from './TodoItem';

export default {
    name: "Todos",
    components: {
        TodoItem
    },
    props: ["todos"]
}
</script>

<style scoped>

</style>