<template>
  <div id="app">
    <img src="./assets/logo.png">
    <ol>
      <todo-item v-for="item in groceryList" v-bind:todo="item"></todo-item>
    </ol>
    <hello></hello>
  </div>
</template>

<script>
import Hello from './components/Hello'
import TodoItem from './components/TodoItem'

export default {
  name: 'app',
  components: {
    Hello,
    TodoItem
  },
  data () {
    return {
      groceryList: [
        { text: 'Vegetables' },
        { text: 'Cheese' },
        { text: 'Whatever else humans are supposed to eat' }
      ]
    }
  }
}
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
</style>
