<template>
    <section>
        <h1>Todos</h1>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis, quisquam. Ipsa iste sit accusantium laudantium, cupiditate, animi veniam alias velit quae asperiores quidem excepturi atque eveniet consequatur officiis natus aut!</p>
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