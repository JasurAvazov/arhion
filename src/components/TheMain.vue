<script>
import TheHeader from "./TheHeader.vue";
import TheIntro from "./TheIntro.vue";
import introBg from "../assets/images/jpg/intro.jpg";

import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/effect-fade";
// import required modules
import { EffectFade, Autoplay } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
    TheIntro,
    TheHeader,
  },
  data() {
    return {
      introBg,
    };
  },
  setup() {
    return {
      modules: [EffectFade, Autoplay],
    };
  },
};
</script>

<template>
  <div class="wrapper">
    <div class="wrapper-bg">
      <swiper
        :effect="'fade'"
        :modules="modules"
        :autoplay="{
          delay: 3500,
          disableOnInteraction: false,
        }"
        :loop="true"
        class="mySwiper"
      >
        <swiper-slide>
          <img :src="introBg" />
        </swiper-slide>
        <swiper-slide>
          <img src="https://swiperjs.com/demos/images/nature-3.jpg" />
        </swiper-slide>
      </swiper>
    </div>
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
    height: 100%;
  }
  &-bg {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;
    overflow: hidden;
  }
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  animation-name: zoom;
  animation-duration: 50s;
  animation-fill-mode: forwards;
}

@keyframes zoom {
  from {
    transform: scale(1);
  }

  to {
    transform: scale(2.5);
  }
}
</style>
