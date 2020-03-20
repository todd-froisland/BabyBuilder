<template>
  <div id="app">
    <div id = "header">
      <p>Baby Builder</p>
    </div>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/store">Cart</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'App',
  created() {
    console.log("help");
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#header {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80px;
  background-color: #FFB28A;
  font-size: 50px;
  font-family: 'Liu Jian Mao Cao', cursive;
  font-weight: bold;

}

#nav {
  padding: 30px;
}

#nav a {
  font-family: 'Liu Jian Mao Cao', cursive;
  font-size: 30px;
  font-weight: bold ;
  text-decoration: none;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
