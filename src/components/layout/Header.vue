<template>
  <div id="Header">
    <div id="banner">To Do List</div>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  #banner {
    color: red;
    background: lightgray;
    font-size: 2em;
  }
</style>