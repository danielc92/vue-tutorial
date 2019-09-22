<template>
    <div class="todo-box">
        <div class="space-between-container">
            <div>
                <h3 class="todo-title">{{ todo.title }}</h3>
            </div>
            <div>
                <p 
        class='status-tag'
        v-bind:class="[ todo.completed ? 'complete' : 'incomplete']">
        {{ todo.completed ? 'Completed' : 'Incomplete' }}
        </p>
            </div>
        </div>
        
        <p class="todo-para">Ad id laboisi deserunt qui ure et. Cillum nostrud velit commodo consectetur adipisicing irure consequat consectetur ipsum aliquip velit reprehenderit ipsum voluptate. Commodo fugiat id incididunt labore laborum sunt velit amet tempor voluptate.</p>
        <p>{{ todo.task }}</p>
        <p class="userid-para">Created by user with id {{ todo.userId }}.</p>
        <p v-if="!todo.completed" class="todo-reminder"><strong>alert!</strong> You may need to work on this task soon...</p>
        
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
        padding: 1.2rem 2rem;
        border: 1px solid rgba(172, 152, 152, 0.2);
    }

    .space-between-container {
        display: flex;
        justify-content: space-between;
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
        color: white;
        padding: .4rem;
        border-radius: 4px;
        font-size: .8rem;
        text-transform: lowercase;
        border: none;
    }

    .incomplete {
        color: rgba(205, 37, 74, 1);
        border: .1rem solid rgba(205, 37, 74, 1);
    }
    .complete {
        color: rgba(65, 192, 72, .8);
        border: .1rem solid rgba(65, 192, 72, .5);
    }

    .todo-reminder {
        display: inline-block;
        padding: 1rem;
        background: white;
        border-radius: 5px;
        color: red;
        border: .1rem solid red;
        background-color: rgba(255,0,0,.1);
    }
</style>