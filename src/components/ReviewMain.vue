<template>
  <div class="container">
    <div class="label">
      <div class="label text">Мой отзыв</div>
      <div class="label close"></div>
    </div>
    <hr />
    <div class="picture">
      <img src="../assets/mainpic1.jpg" />
      <div class="picture text">
        <h1 class="picture text header">Фоточки в свадебном платьице</h1>
        <p class="picture text author">Алена Смирнова</p>
      </div>
    </div>
    <div class="starsection">
      <StarElement title="Скорость"></StarElement>
      <StarElement title="Скорость отдачи видео"></StarElement>
      <StarElement title="Качество"></StarElement>
      <StarElement title="Пунктуальность"></StarElement>
    </div>
    <CommentSection></CommentSection>
    <Gallery></Gallery>
    <hr class="separateline" />
    <button class="submitbutton">Отправить</button>
  </div>
</template>
<script>
import StarElement from "./StarElement";
import CommentSection from "./CommentSection";
import Gallery from "./Gallery";

export default {
  components: { StarElement, CommentSection, Gallery },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");
.container {
  background: #ffffff;
  width: 560px;
  height: 656px;
  border-radius: 16px;

  hr {
    opacity: 0.2;
  }
  .label {
    display: flex;
    height: 48px;
    .text {
      font-family: "Montserrat", sans-serif;
      font-weight: 600;
      float: left;
      margin-left: 32px;
      margin-top: 19px;
    }
    .close {
      position: absolute;
      left: 540px;
      margin-top: 21px;
      width: 25px;
      height: 25px;
      opacity: 0.3;
    }
    .close:hover {
      opacity: 1;
    }
    .close:before,
    .close:after {
      position: absolute;
      content: " ";
      height: 18px;
      width: 2px;
      background-color: #333;
    }
    .close:before {
      transform: rotate(45deg);
    }
    .close:after {
      transform: rotate(-45deg);
    }
  }
  .picture {
    display: flex;
    img {
      border-radius: 6px;
      width: 102px;
      height: 68px;
      margin-left: 32px;
      margin-top: 14px;
    }
    .text {
      font-family: "Montserrat", sans-serif;
      display: flex;
      flex-direction: column;
      .header {
        margin: 0;

        font-weight: 600;
        font-size: 16px;
        margin-top: 30px;
        margin-left: 20px;
      }
      p {
        margin: 0;
        font-weight: 400;
        font-size: 12px;
        margin-left: 20px;
        margin-top: 5px;
      }
    }
  }
  .starsection {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 403px;
    margin-left: 30px;
    margin-top: 10px;
  }
  .separateline {
    margin-top: 26px;
  }
  .submitbutton {
    border: none;
    width: 105px;
    height: 36px;
    min-width: 40px;
    border-radius: 6px;
    margin-right: 16px;
    margin-top: 5px;
    float: right;
    text-decoration: none;
    background: #53c6d1;
    color: #ffffff;

    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    font-size: 0.85rem;
    line-height: 1;
    cursor: pointer;
    text-align: center;
    transition: background 250ms ease-in-out, transform 150ms ease;
    -webkit-appearance: none;
    -moz-appearance: none;
  }
}
</style>
