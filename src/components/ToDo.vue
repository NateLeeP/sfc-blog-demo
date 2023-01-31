<template>
    <div class="todo-container">
        <p :class="{ strikethrough: toDo.complete }">
            {{ toDo.text }}
        </p>
        <input type="checkbox" @click="() => $emit('toggle-to-do', toDo)" />
    </div>
</template>
<script>
export default {
    props: {
        toDo: Object
    }
}
</script>
<style>
.todo-container {
    display: flex;
    justify-content: space-between;
    max-width: 250px;
    margin: 0 auto;
}

.strikethrough {
    text-decoration: line-through;
}
</style>