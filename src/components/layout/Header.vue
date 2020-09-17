<template>
  <header class="header">
    <h1>TodoList</h1>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name:"header"
}
</script>

<style scoped>
  .header{
    color: #fff;
    background: #333;
    text-align: center;
    padding: 10px;
  }
  
  .header a {
    color:#fff;
    padding:0 5px;
    text-decoration: none;
  }

  .header h1 {
    margin:0.1em 0;
  }
</style>