<template>
  <div class="home">
    <AddTodo @add-todo="addTodo" />
    <Todos :todos="todos" @del-todo="deltodo" />
  </div>
</template>

<script>
// @ is an alias to /src
import AddTodo from '@/components/AddTodo.vue'
import Todos from '@/components/Todos.vue'
import axios from 'axios'
export default {
  name: 'Home',
  data() {
    return {
      todos: [
      ]
    }
  },
  methods: {
    deltodo(id) {
      axios.delete(`https://jsonplaceholder.typicode.com/todos/${id}`)
      .then(res => this.todos=this.todos.filter(todo => todo.id !== id))
      .catch(err => console.log(err))
          },
    addTodo(newItem) {
      const {title, completed} = newItem;
      axios.post('https://jsonplaceholder.typicode.com/todos', {title,completed})
      .then(res => this.todos=[...this.todos,newItem])
      .catch(err => console.log(err))
    }
  },
  components: {
    AddTodo,
    Todos
  },
  created() {
    axios.get('https://jsonplaceholder.typicode.com/todos?_limit=5')
    .then(res => this.todos = res.data)
    .catch(error => console.log(error))
  }
}
</script>
