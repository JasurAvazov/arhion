<template>
  <section class="whyus">
    <div class="container">
      <h2 class="whyus-title">Вместе с нами вы</h2>
      <div class="whyus__slider">
        <swiper
          :direction="'vertical'"
          :modules="modules"
          :autoplay="{
            delay: 4500,
            disableOnInteraction: false,
          }"
          :allow-touch-move="false"
          :loop="true"
          class="mySwiper"
        >
          <swiper-slide
            v-for="(item, index) in swiperData"
            :key="index"
          >
            <h3 class="whyus__slider-title">{{ item.title }}</h3>
            <ul class="whyus__slider-list">
              <li
                class="whyus__slider-item"
                v-for="(el, index) in item.content"
                :key="index"
              >
                {{ el }}
              </li>
            </ul>
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Autoplay } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiperData: [
        {
          title: "делегируете",
          content: [
            "контроль качества строительсва",
            "Задачи, в которых вы не разбираетесь",
            "По подбору и закупке материалов",
            "Архитектурный надзор за строительством",
          ],
        },
        {
          title: "сохраняете",
          content: ["Время", "Силы", "Нервы", "Деньги"],
        },
        {
          title: "контролируете",
          content: [
            "Вопросы, которые для вас важны",
            "На какой стадии находится строительство",
            "Вопросы, в которых важно ваше мнение",
          ],
        },
        {
          title: "счастливы",
          content: [
            "Воплощать свои мечты",
            "Ощущать безопасность за результат",
            "Быть уверенными в нашей поддержке",
          ],
        },
      ],
    };
  },
  setup() {
    return {
      modules: [Autoplay],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.whyus {
  background-color: $gray;
  padding: 60px 0 120px;
  .container {
    display: flex;
    align-items: flex-start;
    gap: 18px;
  }
  &-title {
    color: $primary-white;
    font-family: "Inter";
    font-size: 44px;
    font-weight: 400;
    line-height: 50px;
    width: 400px;
  }

  &__slider {
    height: 350px;
    width: calc(100% - 400px);
    &-title {
      color: $gold;
      font-family: "Inter";
      font-size: 44px;
      font-weight: 600;
      line-height: 50px;
    }
    &-list {
      margin-top: 30px;
      display: flex;
      flex-direction: column;
      gap: 30px;
    }
    &-item {
      color: $primary-white;
      font-family: "Inter";
      font-size: 35px;
      font-weight: 400;
      padding-left: 25px;
      position: relative;
      &::before {
        content: "";
        position: absolute;
        left: -15px;
        border-radius: 16px;
        background: $gold;
        width: 25px;
        height: 8px;
        top: 50%;
        transform: translateY(-25%);
      }
    }
  }
}

.swiper {
  width: 100%;
  height: 100%;
  overflow-x: visible;
}

.swiper-slide {
  display: flex;
  flex-direction: column;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
