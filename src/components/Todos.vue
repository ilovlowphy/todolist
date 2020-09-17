<template>
  <div>
    <!-- <TodoItem v-for="todo in todos" :todo="todo"/> -->
    hello
  </div>
</template>

<script>
import TodoItem from "@/components/TodoItem.vue"
export default {
  name: Todos,
  props: ["todos"],
  components: {
      TodoItem
  }
}
</script>

<style>

</style>