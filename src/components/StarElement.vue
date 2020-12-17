<template>
  <div class="starblock">
    <div class="starblock label">
      {{ title }}
    </div>
    <div class="starblock stars">
      <span
        v-for="star in stars"
        :key="star.n"
        v-bind:class="{ active: star.active }"
        @click="activateStars(star.n)"
      ></span>
      <!-- <span class="active"></span>
      <span class="active"></span>
      <span class="active"></span>
      <span></span>
      <span></span> -->
    </div>
  </div>
</template>

<script>
export default {
  props: ["title"],
  data() {
    return {
      stars: [
        {
          n: 0,
          active: false,
        },
        {
          n: 1,
          active: false,
        },
        {
          n: 2,
          active: false,
        },
        {
          n: 3,
          active: false,
        },
        {
          n: 4,
          active: false,
        },
      ],
    };
  },
  methods: {
    activateStars(n) {
      for (let i = 0; i < this.stars.length; i++) {
        this.stars[i].active = false;
      }
      for (let i = 0; i <= n; i++) {
        this.stars[i].active = true;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600&display=swap");
.starblock {
  display: flex;
  flex-direction: column;
  width: 180px;
  margin-top: 24px;
  .label {
    font-family: "Montserrat", sans-serif;
    font-size: 14px;
    font-weight: 500;
    margin: 0;
  }
  .stars {
    width: 165px;
    margin: 0;
    margin-top: 7px;
    padding-left: 2px;
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    span {
      padding: 0;
      font-size: 32px;
      margin: 0;
      line-height: 1;
      color: lightgrey;
    }
    > span:before {
      content: "★";
    }
    > span.active {
      color: #53c6d1;
    }
  }
}
</style>
