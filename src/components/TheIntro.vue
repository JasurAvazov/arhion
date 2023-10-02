<template>
    <div class="intro">
        <div class="container">
            <div class="intro-content">
                <div class="intro-image">
                    <img
                        :src="introImage"
                        alt="intro image"
                    >
                </div>
                <h3 class="intro-subtitle">
                    Строим, проектируем и наполняем смыслами
                </h3>
            </div>
            <div class="intro__btn">
                <div class="intro__btn-content">
                    ПОДОБРАТЬ ПРОЕКТ
                </div>
                <div class="intro__btn-arrow">
                    <img
                        :src="introArrow"
                        alt="arrow right"
                    >
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import introImage from '../assets/images/png/intro.png'
import introArrow from '../assets/images/svg/right-arrow.svg'
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.intro {
    margin-top: 72px;

    .container {
        max-width: 1300px;
    }

    &-content {
        max-width: 1100px;
        width: 100%;
        margin: auto;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
    }

    &-image {
        width: 100%;
        padding: 0 30px;

        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    &-subtitle {
        margin-top: 26px;
        color: $primary-white;
        text-shadow: 2px 2px 12px rgba(0, 0, 0, 0.25), -2px -2px 12px rgba(0, 0, 0, 0.25);
        font-family: 'Inter';
        font-size: 30px;
        font-weight: 600;
        line-height: 48px;
        max-width: 357px;
    }

    &__btn {
        margin-top: -20px;
        display: flex;
        align-items: center;
        gap: 62px;

        &-content {
            cursor: pointer;
            width: 180px;
            height: 180px;
            border-radius: 50%;
            background-color: $white;
            display: flex;
            align-items: center;
            justify-content: center;
            padding-left: 20px;
            color: $gray;
            font-family: 'Montserrat';
            font-size: 22px;
            font-weight: 400;
            line-height: 40px;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                width: 280px;
                height: 2px;
                background-color: $gold;
                top: 50%;
                transform: translateY(-50%);
                left: 20px;
                box-shadow: 1px 1px 7px rgba(0, 0, 0, 0.25), -1px 1px 2px rgba(0, 0, 0, 0.25);
            }
        }

        &-arrow {
            cursor: pointer;
            width: 65px;
            height: 18px;
            transform: translateY(-16px);

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }
    }
}
</style>