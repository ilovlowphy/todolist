<template>
  <div class="todo-item" :key="todo.id" :class="{'is-completed': todo.completed}">
      <p>
        <input type="checkbox" @change="markComplete" :checked="todo.completed">
        {{todo.title}}
        <button class="del" @click="$emit('del-todo',todo.id)">X</button>
      </p>
  </div>
</template>

<script>
export default {
  props:["todo"],
  methods:{
      markComplete() {
          this.todo.completed = !this.todo.completed;
      }
  }
}
</script>

<style scoped>
.todo-item {
    background-color: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
}
.del {
    background-color: red;
    color: #fff;
    border: none;
    padding:5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
}
.is-completed {
    text-decoration: line-through;
}
</style>