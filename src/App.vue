<template>
  <div id="app">
    <global-nav />
    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>

<script>
import GlobalNav from "@/components/GlobalNav";

export default {
  name: "App",
  components: {
    GlobalNav
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0;
  margin: 0;
}
ul li {
  list-style: none;
}
a {
  text-decoration: none;
}
</style>
