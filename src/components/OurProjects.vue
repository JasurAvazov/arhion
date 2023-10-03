<template>
    <section class="projects">
        <div class="container">
            <h2 class="projects-title">
                АКЦИОННЫЕ ПРОЕКТЫ ДОМОВ
            </h2>
            <div class="projects-subtitle">
                Проекты готовые проекты
            </div>
            <ul class="projects__list">
                <li class="projects__list-item">
                    <div class="item-image">
                        <swiper
                            :modules="modules"
                            :slides-per-view="1"
                            :pagination="{
                                clickable: true,
                            }"
                            :loop="true"
                            class="mySwiper"
                        >
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                        </swiper>
                    </div>
                    <div class="item-discounted">
                        %
                    </div>
                    <div class="item-content">
                        <div class="item-header">
                            <h4 class="item-name">ZX76</h4>
                            <div class="item-info">
                                <div class="item-room">
                                    <div class="item-bed">
                                        <img
                                            :src="bedIcon"
                                            alt="bed icon"
                                        >
                                        4
                                    </div>
                                    <div class="item-bath">
                                        <img
                                            :src="bathIcon"
                                            alt="bed icon"
                                        >
                                        2
                                    </div>
                                </div>
                                <div class="item-size">
                                    20×15 м
                                </div>
                                <div class="item-area">
                                    744 м²
                                </div>
                            </div>
                            <div class="item-like">
                                <img
                                    :src="likeIcon"
                                    alt="like icon"
                                >
                            </div>
                        </div>
                        <ul class="prices__list">
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость строительства от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">10 800 000 ₽</h5>
                                    <h5 class="prices__list-discount">10 800 000 ₽</h5>
                                </div>
                            </li>
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость проекта от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">45 000 ₽</h5>
                                    <h5 class="prices__list-discount">45 000 ₽</h5>
                                </div>
                            </li>
                        </ul>
                    </div>

                </li>
                <li class="projects__list-item">
                    <div class="item-image">
                        <swiper
                            :modules="modules"
                            :slides-per-view="1"
                            :pagination="{
                                clickable: true,
                            }"
                            :loop="true"
                            class="mySwiper"
                        >
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                        </swiper>
                    </div>
                    <div class="item-discounted">
                        %
                    </div>
                    <div class="item-content">
                        <div class="item-header">
                            <h4 class="item-name">ZX76</h4>
                            <div class="item-info">
                                <div class="item-room">
                                    <div class="item-bed">
                                        <img
                                            :src="bedIcon"
                                            alt="bed icon"
                                        >
                                        4
                                    </div>
                                    <div class="item-bath">
                                        <img
                                            :src="bathIcon"
                                            alt="bed icon"
                                        >
                                        2
                                    </div>
                                </div>
                                <div class="item-size">
                                    20×15 м
                                </div>
                                <div class="item-area">
                                    744 м²
                                </div>
                            </div>
                            <div class="item-like">
                                <img
                                    :src="likeIcon"
                                    alt="like icon"
                                >
                            </div>
                        </div>
                        <ul class="prices__list">
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость строительства от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">10 800 000 ₽</h5>
                                    <h5 class="prices__list-discount">10 800 000 ₽</h5>
                                </div>
                            </li>
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость проекта от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">45 000 ₽</h5>
                                    <h5 class="prices__list-discount">45 000 ₽</h5>
                                </div>
                            </li>
                        </ul>
                    </div>
                </li>
                <li class="projects__list-item">
                    <div class="item-image">
                        <swiper
                            :modules="modules"
                            :slides-per-view="1"
                            :pagination="{
                                clickable: true,
                            }"
                            :loop="true"
                            class="mySwiper"
                        >
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                        </swiper>
                    </div>
                    <div class="item-discounted">
                        %
                    </div>
                    <div class="item-content">
                        <div class="item-header">
                            <h4 class="item-name">ZX76</h4>
                            <div class="item-info">
                                <div class="item-room">
                                    <div class="item-bed">
                                        <img
                                            :src="bedIcon"
                                            alt="bed icon"
                                        >
                                        4
                                    </div>
                                    <div class="item-bath">
                                        <img
                                            :src="bathIcon"
                                            alt="bed icon"
                                        >
                                        2
                                    </div>
                                </div>
                                <div class="item-size">
                                    20×15 м
                                </div>
                                <div class="item-area">
                                    744 м²
                                </div>
                            </div>
                            <div class="item-like">
                                <img
                                    :src="likeIcon"
                                    alt="like icon"
                                >
                            </div>
                        </div>
                        <ul class="prices__list">
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость строительства от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">10 800 000 ₽</h5>
                                    <h5 class="prices__list-discount">10 800 000 ₽</h5>
                                </div>
                            </li>
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость проекта от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">45 000 ₽</h5>
                                    <h5 class="prices__list-discount">45 000 ₽</h5>
                                </div>
                            </li>
                        </ul>
                    </div>
                </li>
                <li class="projects__list-item">
                    <div class="item-image">
                        <swiper
                            :modules="modules"
                            :slides-per-view="1"
                            :pagination="{
                                clickable: true,
                            }"
                            :loop="true"
                            class="mySwiper"
                        >
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                            <swiper-slide>
                                <img
                                    :src="projectItem"
                                    alt="project image"
                                >
                            </swiper-slide>
                        </swiper>
                    </div>
                    <div class="item-discounted">
                        %
                    </div>
                    <div class="item-content">
                        <div class="item-header">
                            <h4 class="item-name">ZX76</h4>
                            <div class="item-info">
                                <div class="item-room">
                                    <div class="item-bed">
                                        <img
                                            :src="bedIcon"
                                            alt="bed icon"
                                        >
                                        4
                                    </div>
                                    <div class="item-bath">
                                        <img
                                            :src="bathIcon"
                                            alt="bed icon"
                                        >
                                        2
                                    </div>
                                </div>
                                <div class="item-size">
                                    20×15 м
                                </div>
                                <div class="item-area">
                                    744 м²
                                </div>
                            </div>
                            <div class="item-like">
                                <img
                                    :src="likeIcon"
                                    alt="like icon"
                                >
                            </div>
                        </div>
                        <ul class="prices__list">
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость строительства от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">10 800 000 ₽</h5>
                                    <h5 class="prices__list-discount">10 800 000 ₽</h5>
                                </div>
                            </li>
                            <li class="prices__list-item">
                                <h4 class="prices__list-title">Стоимость проекта от:</h4>
                                <div class="prices__list-content">
                                    <h5 class="prices__list-price">45 000 ₽</h5>
                                    <h5 class="prices__list-discount">45 000 ₽</h5>
                                </div>
                            </li>
                        </ul>
                    </div>

                </li>
            </ul>
        </div>
    </section>
</template>

<script>
import projectItem from '../assets/images/jpg/projectItem.jpg';
import likeIcon from '../assets/images/svg/like.svg';
import bedIcon from '../assets/images/svg/bed.svg';
import bathIcon from '../assets/images/svg/bath.svg';

import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

import { Pagination } from 'swiper/modules';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    data() {
        return {
            projectItem: projectItem,
            likeIcon: likeIcon,
            bedIcon: bedIcon,
            bathIcon: bathIcon
        }
    },
    setup() {
        return {
            modules: [Pagination],
        };
    },
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.projects {
    padding: 120px 0;

    &-title {
        color: rgba(167, 139, 115, 0.10);
        text-align: left;
        font-family: 'Inter';
        font-size: 84px;
        line-height: 86px;
        font-weight: 700;
        text-transform: uppercase;
    }

    &-subtitle {
        color: $gray;
        font-family: 'Inter';
        font-size: 48px;
        font-weight: 400;
        line-height: 56px;
        margin-top: -30px;
    }

    &__list {
        margin-top: 40px;
        display: flex;
        flex-wrap: wrap;
        gap: 30px;

        &-item {
            width: calc(50% - 15px);
            position: relative;
            background-color: $primary-white;
            box-shadow: 0px 0px 12px 0px rgba(0, 0, 0, 0.15);
        }
    }
}

.item {
    &-image {
        width: 100%;
        height: 420px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    &-discounted {
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        border: 2px solid $gold;
        background: $primary-white;
        color: $black;
        font-family: 'Montserrat';
        font-size: 24px;
        font-weight: 500;
        line-height: 28px;
        position: absolute;
        z-index: 2;
        left: -9px;
        top: -9px;
    }

    &-content {
        padding: 0 20px 32px;
        display: flex;
        flex-direction: column;
        gap: 24px;
    }

    &-header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 8px;
    }

    &-name {
        color: $black;
        font-family: 'Montserrat';
        font-size: 24px;
        font-weight: 500;
        line-height: 28px;
    }

    &-like {
        width: 30px;
        height: 30px;
        cursor: pointer;

        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    &-info {
        display: flex;
        gap: 20px;
        align-items: center;
        color: $black;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 400;
        line-height: 26px;
    }

    &-room {
        display: flex;
        gap: 8px;
        align-items: center;

        &>div {
            display: flex;
            align-items: center;
            gap: 4px;
        }
    }
}

.prices__list {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    gap: 16px;

    &-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 12px;
    }

    &-title {
        color: $black;
        font-family: 'Montserrat';
        font-size: 18px;
        font-weight: 600;
        line-height: 26px;
    }

    &-content {
        display: flex;
        align-items: center;
        gap: 12px;
    }

    &-price {
        color: $black;
        font-family: 'Montserrat';
        font-size: 14px;
        font-weight: 400;
        line-height: 18px;
        text-decoration-line: line-through;
    }

    &-discount {
        color: $gold;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 700;
        line-height: 26px;
    }
}

.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {
    background: $white;
    display: flex;
    justify-content: center;
    align-items: center;
    height: calc(100% - 30px);
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>

<style lang="scss">
.swiper-pagination-bullet-active {
    background-color: #969696 !important;
}

.swiper-pagination-bullet {
    width: 24px;
    border-radius: 16px;
    height: 4px;
    background-color: #D8D8D8 !important;
}
</style>