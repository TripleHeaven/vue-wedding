<template>
  <div class="container">
    <div class="label">
      <div class="label text">Новый отзыв</div>
      <div class="label close"></div>
    </div>

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
    <hr class="separateline" />
    <button class="submitbutton" @click="submitForm">Продолжить</button>
  </div>
</template>
<script>
import StarElement from "./StarElement";

export default {
  components: { StarElement },
  methods: {
    submitForm() {
      alert("Вы успешно оставили комментарий!");
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");
.container {
  background: #ffffff;
  width: 320px;
  height: 573px;
  border-radius: 16px 16px 0px 0px;
  margin-left: 10px;
  margin-top: 10px;
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
      margin-left: 16px;
      margin-top: 19px;
    }
    .close {
      position: absolute;
      left: 860px;
      margin-top: 19px;
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
    flex-direction: column;
    img {
      border-radius: 6px;
      width: 84px;
      height: 56px;
      margin-left: 16px;
      margin-top: 7px;
    }
    .text {
      font-family: "Montserrat", sans-serif;
      display: flex;
      flex-direction: column;
      .header {
        margin: 0;

        font-weight: 600;
        font-size: 16px;
        margin-top: 18px;
        margin-left: 17px;
      }
      p {
        margin: 0;
        font-weight: 400;
        font-size: 12px;
        margin-left: 17px;
        margin-top: 5px;
      }
    }
  }
  .starsection {
    display: flex;
    flex-direction: column;

    justify-content: space-between;

    margin-left: 16px;
    margin-top: 3px;
    #block {
      margin-bottom: -5px;
    }
  }
  .separateline {
    margin-top: 30px;
  }
  .submitbutton {
    border: none;
    width: 120px;
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
