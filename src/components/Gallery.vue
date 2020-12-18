<template>
  <div class="gallery">
    <div class="galleryelement">
      +
    </div>
    <img src="../assets/lilpic1.jpg" />
    <img src="../assets/lilpic2.jpg" />
    <img src="../assets/lilpic3.jpg" />
    <img src="../assets/lilpic4.jpg" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.gallery {
  margin-right: auto;
  margin-left: 32px;
  margin-top: 16px;
  display: flex;
  width: 77%;
  justify-content: space-between;
  .galleryelement {
    width: 80px;
    height: 80px;
    border-radius: 6px;
    background: #f3f4f6;
    text-align: center;
    line-height: 80px;
    color: #9aa2b7;
    font-size: 25px;
  }
  img {
    width: 80px;
    height: 80px;
    border-radius: 6px;
  }
}
</style>
