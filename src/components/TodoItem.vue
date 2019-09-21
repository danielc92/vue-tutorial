<template>
    <div class="todo-box">
        <h2>{{ todo.title }}</h2>
        <p>{{ todo.task }}</p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"]
}
</script>

<style scoped>
    .todo-box {
        background: red;
        color: white;
        border: none;
        border-radius: 2px;
        margin-bottom: 1rem;
        padding: .4rem .3rem;
    }
</style>