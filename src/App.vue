<template>
  <div id="app">
    <ReviewMain></ReviewMain>
    <ReviewSmall></ReviewSmall>
    <ReviewCommentSmall></ReviewCommentSmall>
  </div>
</template>

<script>
import ReviewMain from "./components/ReviewMain";
import ReviewSmall from "./components/ReviewSmall";
import ReviewCommentSmall from "./components/ReviewCommentSmall";
export default {
  name: "App",
  components: { ReviewMain, ReviewSmall, ReviewCommentSmall },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #ebedf0;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
}
</style>
