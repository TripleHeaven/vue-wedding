<template>
  <div class="container">
    <div class="label">
      <div class="label text">
        <i class="fas fa-arrow-left"></i> Новый отзыв
      </div>
      <div class="label close"></div>
    </div>
    <hr />
    <div class="inputcontainer">
      <textarea v-model="comment" />
      <div class="inputcontainer quantitylabel">{{ comment.length }}/500</div>
    </div>
    <Gallery></Gallery>
    <hr class="separateline" />
    <button class="submitbutton" @click="submitForm">Отправить</button>
  </div>
</template>
<script>
import Gallery from "./Gallery";
export default {
  components: { Gallery },
  methods: {
    submitForm() {
      alert("Вы успешно оставили комментарий!");
    },
  },
  data() {
    return {
      comment: "Комментарий",
    };
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");
.container {
  background: #ffffff;
  width: 320px;
  height: 624px;
  margin-left: 10px;
  margin-top: 10px;
  .gallery {
    flex-wrap: wrap;
    margin-left: 15px;
    margin-top: 20px;
    width: 80%;
    height: 180px;
  }
  hr {
    opacity: 0.2;
  }
  .label {
    display: flex;
    height: 48px;
    .fa-arrow-left {
      font-size: 16px;
      color: #9aa2b7;
      margin-right: 17px;
    }
    .text {
      font-family: "Montserrat", sans-serif;
      font-weight: 600;
      float: left;
      margin-left: 19px;
      margin-top: 20px;
    }
    .close {
      position: absolute;
      left: 1180px;
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
    margin-top: 124px;
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
  .inputcontainer {
    display: flex;
    flex-direction: column;

    margin-top: 12px;
    textarea {
      width: 288px;
      height: 146px;
      padding: 10px;
      margin-left: auto;
      margin-right: auto;
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
      width: 55px;
      font-family: "Montserrat", sans-serif;
      font-size: 12px;
      color: #7f899e;
    }
  }
}
</style>
