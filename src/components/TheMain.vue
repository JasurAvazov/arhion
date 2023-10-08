<script setup>
import TheHeader from "./TheHeader.vue";
import TheIntro from "./TheIntro.vue";

import { ref, onMounted } from "vue";

const wrapper = ref(null);

const wrapperIsActive = ref(false);

const backgrounds = ref([
  {
    link: "url(/src/assets/images/jpg/intro.jpg)",
    active: true,
    zoomed: false,
  },
  {
    link: "url(/src/assets/images/jpg/intro.jpg)",
    active: false,
    zoomed: false,
  },
  {
    link: "url(/src/assets/images/jpg/intro.jpg)",
    active: false,
    zoomed: false,
  },
]);


const currentBackgroundIndex = ref(0);

const changeBackground = (items) => {
  let id = currentBackgroundIndex.value;
  items[id].style.backgroundImage = backgrounds.value[id].link;

  backgrounds.value.map((el) => (el.active = false));
  backgrounds.value.map((el) => (el.zoomed = false));
  backgrounds.value[id].active = true;
  backgrounds.value[id].zoomed = true;

  currentBackgroundIndex.value =
    (currentBackgroundIndex.value + 1) % backgrounds.value.length;
  console.log("hello");

  setTimeout(() => {
    changeBackground(items);
  }, 4000);
};

onMounted(() => {
  let items = document.querySelectorAll(".wrapper-bg");

  changeBackground(items);
});
</script>

<template>
  <div class="wrapper">
    <div
      v-for="(item, index) in backgrounds"
      :key="index"
      ref="wrapper"
      class="wrapper-bg"
      :class="{ zoomed: item.zoomed, active: item.active }"
    ></div>
    <div class="container">
      <TheHeader></TheHeader>
      <TheIntro></TheIntro>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.wrapper {
  width: 100%;
  height: 90vh;
  position: relative;
  overflow: hidden;
  .container {
    position: relative;
    z-index: 2;
  }
  &-bg {
    background-image: url("../assets/images/jpg/intro.jpg");
    background-size: cover;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    opacity: .2;
    transition: transform 3s ease, 0.4s opacity;
    &.active {
      opacity: 1;
      z-index: 1;
    }
    &.zoomed {
      transform: scale(1.2); /* Увеличение при анимации */
    }
  }
}
</style>
