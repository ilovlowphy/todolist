<template>
  <header class="header">
    <h1>To Do List</h1>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
    color: #fff;
    background: #555;
    text-align: center;
  }

.header h1 {
  margin: 0;
}

#nav a {
  color: #fff;
  padding: 0 5px;
  text-decoration: none;
}
</style>