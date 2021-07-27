<template>
  <div id="app">
    <nav>
      <router-link class="link" to="/">Home</router-link>
      <router-link class="link" to="/myBooks"> MyBooks</router-link>
    </nav>
    <router-view />
    <nav>
      <router-link class="link" to="/addBook"> Add book</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px;
}

.link {
  text-decoration: none;
  margin-left: 20px;
  font-weight: 700;
}
</style>
