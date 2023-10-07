<template>
  <div class="review">
    <div class="container">
      <div class="review-logo">
        <img
          :src="reviewLogo"
          alt=" review logo"
        />
      </div>
      <h2 class="review-title">О нас</h2>
      <h3 class="review-subtitle">обзор компании</h3>
      <div class="review-bottom">
        <a
          href="#"
          class="review__btn"
        >
          <p class="review__btn-text">НАЧАТЬ</p>
          <div class="review__btn-arrow">
            <img
              :src="arrowIcon"
              alt="arrow icon"
            />
          </div>
        </a>
        <div class="review__mark">
          <div class="review__mark-img">
            <img
              :src="commitetLogo"
              alt="commitet image"
            />
          </div>
          <p class="review__mark-text">
            Возглавляем Комитет МТПП по предпринимательству в сфере архитектуры,
            проектирования и строительства
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import arrowIcon from "../assets/images/svg/gray-arrow-small.svg";
import reviewLogo from "../assets/images/png/reviewLogo.png";
import commitetLogo from "../assets/images/png/commitet.png";
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.review {
  padding: 45px 0 60px;
  background: rgba(241, 235, 230, 0.72);
  position: relative;

  &-logo {
    width: 288px;
    height: 108px;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  &-title {
    position: absolute;
    color: rgba(167, 139, 115, 0.1);
    font-family: "Inter";
    font-size: 330px;
    font-weight: 700;
    text-transform: uppercase;
    top: 65px;
    right: 7%;
  }

  &-subtitle {
    margin-top: 130px;
    color: $gold;
    font-family: "Inter";
    font-size: 165px;
    font-weight: 400;
    text-transform: uppercase;
  }

  &-bottom {
    margin-top: 55px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }

  &__btn {
    display: flex;
    align-items: center;
    gap: 100px;
    cursor: pointer;
    padding-bottom: 25px;

    &:hover {
      .review__btn-arrow {
        background-color: $gold;
        transition: 0.3s all;
      }
    }
    &-text {
      font-family: "Montserrat";
      color: $black;
      font-size: 34px;
      font-style: normal;
      font-weight: 400;
      line-height: 26px;
      position: relative;

      &::after {
        content: "";
        position: absolute;
        height: 1px;
        width: 300px;
        background: $gray;
        left: 0;
        top: 115%;
        z-index: 2;
      }
    }

    &-arrow {
      transition: 0.3s all;
      cursor: pointer;
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 1px solid $gray;
      display: flex;
      justify-content: center;
      align-items: center;
      transform: translateY(15px);

      img {
        width: 35px;
        height: 20px;
        transform: translate(-210%, -35%);
      }
    }
  }

  &__mark {
    display: flex;
    gap: 22px;
    align-items: center;

    &-img {
      width: 94px;
      height: 120px;

      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
      }
    }

    &-text {
      color: $gray;
      font-family: "Montserrat";
      font-size: 24px;
      font-weight: 500;
      line-height: 30px;
      max-width: 600px;
    }
  }
}
</style>
