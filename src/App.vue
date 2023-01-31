<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <ToDoList :toDoList="todos" />
</template>

<script>
import ToDoList from './components/ToDoList.vue'

export default {
  name: 'App',
  components: {
    ToDoList
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          text: 'Wash the car',
          complete: false
        },
        {
          id: 2,
          text: "Brush my teeth",
          complete: false
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
