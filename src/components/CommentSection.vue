<template>
  <div class="inputcontainer">
    <textarea v-model="comment" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      comment: "Комметарий",
    };
  },
};
</script>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");
.inputcontainer {
  width: 496px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
  textarea {
    width: 496px;
    height: 100px;
    background: #fafafa;
    border: 1px solid #eaecf0;
    box-sizing: border-box;
    border-radius: 6px;
    resize: none;
    font-family: "Montserrat", sans-serif;
    font-weight: 500;
    font-size: 16px;
  }
}
</style>
