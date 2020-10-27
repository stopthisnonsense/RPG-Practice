<template>
  <div class="nav">
    <router-link v-for="route in routes" :key="route.path" :to="route.path">{{
      route.name
    }}</router-link>
  </div>
</template>
<script>
export default {
  name: "Navigation",
  props: {},
  data() {
    return {
      routes: this.$router.options.routes
    };
  }
};
// import Routes from "@/router/index.js";
// console.log(Routes.getRoutes());
</script>

<style scoped lang="scss">
.nav {
  padding: 30px;
  display: flex;
  justify-content: center;

  a {
    display: block;
    padding: 0.5rem;
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
