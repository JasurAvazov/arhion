<template>
    <section class="dostep">
        <div class="container">
            <h2 class="dostep-title">
                нужен проект
            </h2>
            <h3 class="dostep-subtitle">
                Индвидуальное проектирование
            </h3>
            <p class="dostep-article">
                Продолжить вдохновляться - перейдите на страницу индивидуального проектирования, где вы сможете сделать
                каждую деталь вашего будущего дома выразительной, олицетворяющей вас. Откройте двери в мир творчества и
                возможностей.
            </p>
            <div class="dostep__btn">
                <p class="dostep__btn-text">Воплотите свои мечты</p>
                <div class="dostep__btn-arrow">
                    <img
                        :src="arrowGray"
                        alt="arrow"
                    >
                </div>
            </div>
        </div>
        <div class="dostep-bg">
            <div class="filter"></div>
            <img
                :src="dostepBg"
                alt="bg image"
            >
        </div>
    </section>
</template>

<script setup>
import dostepBg from '../assets/images/jpg/dostepBg.jpg';
import arrowGray from '../assets/images/svg/gray-arrow.svg';
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.dostep {
    background-color: $white;
    padding: 60px 0 70px;
    position: relative;

    &-bg {
        height: 100%;
        position: absolute;
        right: 0;
        top: 0;
        bottom: 0;
        width: calc(100% - 700px);

        .filter {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            right: 0;
            left: 0;
            z-index: 2;
            background: linear-gradient(90deg, #FFF 21.83%, rgba(255, 255, 255, 0.00) 100%);
        }

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            right: 0;
            top: 0;
            z-index: 1;
        }
    }

    .container {
        position: relative;
        z-index: 3;
    }

    &-title {
        color: rgba(167, 139, 115, 0.10);
        font-family: 'Inter';
        font-size: 96px;
        font-weight: 700;
        text-transform: uppercase;
        line-height: 96px;
    }

    &-subtitle {
        color: $gray;
        font-family: 'Inter';
        font-size: 42px;
        font-weight: 400;
        line-height: 48px;
        margin-top: -36px;
    }

    &-article {
        margin-top: 40px;
        color: $gray;
        text-align: justify;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 400;
        max-width: 650px;
    }

    &__btn {
        display: flex;
        align-items: center;
        gap: 100px;
        cursor: pointer;
        margin-top: 100px;

        &-text {
            color: $black;
            font-family: 'Montserrat';
            font-size: 36px;
            font-weight: 400;
            line-height: 26px;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                height: 1px;
                width: 620px;
                background: $gray;
                left: 0;
                top: 160%;
            }
        }

        &-arrow {
            cursor: pointer;
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 1px solid $gray;
            display: flex;
            justify-content: center;
            align-items: center;
            transform: translateY(30px);

            img {
                width: 64px;
                height: 20px;
                transform: translate(-40%, -100%);
            }
        }
    }
}
</style>