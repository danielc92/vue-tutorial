<template>
    <div class="todo-box">
        <h3 class="todo-title">{{ todo.title }}</h3>
        <p class="todo-para">Ad id laboisi deserunt qui ure et. Cillum nostrud velit commodo consectetur adipisicing irure consequat consectetur ipsum aliquip velit reprehenderit ipsum voluptate. Commodo fugiat id incididunt labore laborum sunt velit amet tempor voluptate.</p>
        <p>{{ todo.task }}</p>
        <p class="userid-para">Created by user with id {{ todo.userId }}.</p>
        <p v-if="!todo.completed" class="todo-reminder"><strong>alert!</strong> You may need to work on this task soon...</p>
        <p 
        class='status-tag'
        v-bind:class="[ todo.completed ? 'complete' : 'incomplete']">
        {{ todo.completed ? 'Completed' : 'Incomplete' }}
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"]
}
</script>

<style>
    :root {
        --danger: rgb(212, 146, 22);
    }
    .todo-box {
        margin: 0rem auto 1.2rem auto;
        max-width: 700px;
        background: white;
        color: rgba(0,0,0,.9);
        border: none;
        border-radius: 0;
        padding: .4rem 1rem;
        border: 1px solid rgba(172, 152, 152, 0.2);
    }

    .todo-title {
        text-transform: capitalize;
    }

    .userid-para {
        font-size: .9rem;
        color: rgba(0,0,0,.4)
    }

    .todo-para {
        line-height: 1.4rem;
        color: rgba(0,0,0,.7);
    }

    .status-tag {
        display: inline-block;
        color: white;
        padding: .4rem;
        border-radius: 4px;
        font-size: .8rem;
        text-transform: lowercase;
        border: none;
    }

    .incomplete {
        background: rgba(205, 37, 74, 1);
    }
    .complete {
        background: rgba(65, 192, 72, 1);
    }

    .todo-reminder {
        padding: 1rem;
        background: white;
        color: var(--danger);
        border: 1px dotted var(--danger);
    }
</style>