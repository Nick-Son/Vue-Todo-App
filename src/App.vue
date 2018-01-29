<template>
  <div id="app">
    <h1>Vue Todo</h1>
    <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>

<script>

import TodoList from './components/TodoList'

export default {
  name: 'App',
  components: {
    TodoList,
  },

  data() {
    return {
      todos: [
        {
          title: 'Todo A',
          project: 'Project A',
          complete: false,
        },
        {
          title: 'Todo B',
          project: 'Project B',
          complete: false,
        },
        {
          title: 'Todo C',
          project: 'Project C',
          complete: false,
        },
      ]
    }
  }

};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  width: 400px;
  border: 0.5px solid lightgray;
  margin: 10px auto;
  border-radius: 5px;
  padding: 10px;
}
</style>
