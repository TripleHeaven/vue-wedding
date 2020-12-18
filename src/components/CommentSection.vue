<template>
  <div class="inputcontainer">
    <textarea v-model="comment" />
    <div class="inputcontainer quantitylabel">12/500</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      comment: "Комментарий",
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
  margin-top: 28px;
  textarea {
    width: 496px;
    height: 100px;
    padding: 10px;
    padding-top: 15px;
    background: #fafafa;
    border: 1px solid #eaecf0;
    box-sizing: border-box;
    border-radius: 6px;
    resize: none;
    font-family: "Montserrat", sans-serif;
    font-weight: normal;
    font-size: 16px;
  }
  .quantitylabel {
    margin: 0;
    margin-left: auto;
    margin-top: 1px;
    width: 38px;
    font-family: "Montserrat", sans-serif;
    font-size: 12px;
    color: #7f899e;
  }
}
</style>
