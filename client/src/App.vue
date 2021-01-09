<template>
  <div id="app">
    <h1>Todo application</h1>
    <todoList :todos="todos"/>
  </div>
</template>

<script>
import todoList from './components/TodoList'
export default {
  name: 'App',
  data(){
    return{
      todos:[
        {id: 1, title: 'Bred', completed: false},
        {id: 2, title: 'Milk', completed: false},
        {id: 3, title: 'Voter', completed: false},
      ]
    }
  },
  components: {
   todoList
  }
}
</script>
