<template>
  <div id="app">
    {{ todos }}
    <todos v-model="todos"></todos>
    <todos v-model="todos"></todos>
    <button @click="addTodo">Ajouter une tâche</button>
  </div>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
  name: 'App',
  data () {
    return {
      todos: [{
        name: 'Tâche 1',
        completed: true
      }]
    }
  },
  methods: {
    addTodo () {
      this.todos.push({
        name: 'Autre tâche',
        completed: false
      })
    }
  },
  components: {
    Todos
  }
}
</script>
