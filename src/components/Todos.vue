<template>
  <div>
  <div v-for="todo in todos">
    <TodoItem :todo="todo" @del-todo="$emit('del-todo', todo.id)"/>  
  </div>
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem.vue'

export default {
  components: {
      TodoItem
  },
  props: ["todos"]
}
</script>

<style scoped>

</style>