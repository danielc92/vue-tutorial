<template>
    <div class="todo-box">
        <h3>{{ todo.title }}</h3>
        <p class="todo-para">Ad id laboisi deserunt qui ure et. Cillum nostrud velit commodo consectetur adipisicing irure consequat consectetur ipsum aliquip velit reprehenderit ipsum voluptate. Commodo fugiat id incididunt labore laborum sunt velit amet tempor voluptate.</p>
        <p>{{ todo.task }}</p>
        <p class="userid-para">Created by user with id <span class="userid-tag">{{ todo.userId }}</span></p>

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

<style scoped>
    .todo-box {
        margin: .5rem auto .5rem auto;
        max-width: 700px;
        background: white;
        color: rgba(0,0,0,.9);
        border: none;
        border-radius: 0;
        box-shadow: #eee 6px 4px;
        padding: .4rem 1rem;
        border: 1px solid rgba(0,0,0,.1);
    }

    .userid-para {
        font-size: .9rem;
        color: rgba(0,0,0,.4)
    }

    .userid-tag {
        background-color: rgba(0,0,0,.7);
        color: white;
        padding: 0 .4rem;
        border-radius: 4px;
    }

    .todo-para {
        line-height: 1.4rem;
        color: rgba(0,0,0,.7);
    }

    .status-tag {
        display: inline-block;
        color: white;
        padding: .4rem .8rem;
        border: none;
    }

    .incomplete {
        background: rgba(205, 37, 74, 1);
    }
    .complete {
        background: rgba(73, 164, 78, 1);
    }
</style>