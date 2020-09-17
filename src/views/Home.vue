<template>
  <div class="home">
    <AddTodo />
    <Todos :todos="todos"/>
  </div>
</template>

<script>
// @ is an alias to /src
import AddTodo from '@/components/AddTodo.vue'
import Todos from '@/components/Todos.vue'

export default {
  name: 'Home',
  data() {
    return {
      todos:["todo1","todo2"]
    }
  },
  components: {
    AddTodo,
    Todos
  }
}
</script>
