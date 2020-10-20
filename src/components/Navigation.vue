<template>
  <div class="nav">
    <router-link v-for="route in routes" :key="route.path" :to="route.path">{{ route.name }}  |</router-link>
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/other">Other</router-link> -->
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

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
        color: #42b983;
        }
    }
    }
</style>