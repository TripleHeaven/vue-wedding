<template>
  <div id="app">
    <Review></Review>
  </div>
</template>

<script>
import Review from "./components/Review";
export default {
  name: "App",
  components: { Review },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
  margin-top: 60px;
}
</style>
