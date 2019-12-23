<template>
  <div id="nav">
    <router-link to="/">home</router-link>
    <router-link to="/about">about</router-link>
  </div>
</template>

<script>
export default {
  name: "GlobalNav",
  data() {
    return {};
  },
  components: {},
  created() {},
  mounted() {},
  methods: {}
};
</script>
<style scoped>
#nav {
  padding: 30px;
  display: flex;
  justify-content: flex-end;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin-left: 30px;
}

#nav a:hover {
  color: red;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
