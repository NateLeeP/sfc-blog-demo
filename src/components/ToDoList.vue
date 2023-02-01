<template>
    <div class="to-do-container">
        <input v-model="toDoText" />
        <button @click="addTodo">Add To List</button>
        <ToDo v-for="todo in toDos" @toggle-to-do="(toDo) => toDo.complete = !toDo.complete" :toDo="todo"
            :key="todo.text" />
    </div>

</template>
<script>
import ToDo from './ToDo.vue'
export default {
    components: {
        ToDo
    },
    props: {
        toDoList: Array
    },
    data() {
        return {
            toDoText: '',
            toDos: this.toDoList,
        }
    },
    methods: {
        addTodo() {
            this.toDos.push({
                id: this.toDoList.length,
                text: this.toDoText,
                complete: false
            })
        }
    }
}

</script>
<style>

</style>