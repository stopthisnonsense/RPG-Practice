<template>
  <div>
    <Navigation />
    <router-view />
  </div>
</template>
<script>
import Navigation from "@/components/Navigation.vue";
import "@/components/globals.js";
export default {
  components: {
    Navigation
  }
};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
