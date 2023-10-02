<template>
    <section class="service">
        <div class="container">
            <h1 class="service-title">
                СТРОИТЕЛЬСТВО ДОМА ПОД КЛЮЧ
            </h1>
            <h3 class="service-subtitle">Наши услуги</h3>
            <div class="service-content">
                <div class="service-left">
                    <p class="service-text">Предоставим полный комплекс услуг по проектированию и строительству дома.</p>
                    <ul class="service__tabs">
                        <li
                            v-for="item in tabsList  "
                            :key="item.id"
                            class="service__tabs-item"
                            @click="changeTab(item.id)"
                        >
                            <div
                                :class="{ active: item.active }"
                                class="service__tabs-img"
                            >
                                <img
                                    :src="arrow"
                                    alt="arrow"
                                >
                            </div>
                            <h4
                                :class="{ active: item.active }"
                                class="service__tabs-title"
                            >
                                {{ item.title }}
                            </h4>
                        </li>
                    </ul>
                </div>
                <div class="service-right">
                    <div class="service__about">
                        <h3 class="service__about-title">{{ activedTab.title }}</h3>
                        <pre class="service__about-text">
{{ activedTab.text }}
                        </pre>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref, computed } from 'vue';

import arrow from '../assets/images/svg/tabs-arrow.svg';

const tabsList = ref([
    {
        id: 1,
        title: 'Проектирование',
        active: true,
        text: '  Индивидуальный проект дома - это сложный и ответственный процесс, требующий внимания к каждой детали. \n Поэтому, наше архитектурное бюро АРХИОН предоставит и полный спектр услуг от разработки концепции эскизов до подготовки строительной документации и сопровождения проекта.'
    },
    {
        id: 2,
        title: 'Строительство',
        active: false,
        text: '  Выполним, как поэтапное строительство, так и построить дом «под ключ». \n   С нами, вам не придется беспокоиться о поиске строительных материалов, их своевременной доставке или вывозе мусора или контроле строительных операций. \n Позаботимся о строительном надзоре, с соблюдением строительных норм и правил, а так же четких сроков.'
    },
    {
        id: 3,
        title: 'Геология и Геодезия',
        active: false,
        text: ''
    },
    {
        id: 4,
        title: 'Дизайн интерьера',
        active: false,
        text: ' Дизайн проект — это самая творческий и интересный этап. \n   В котором важно учесть не только эстетический стиль дизайн - решения, но и комфорт в последующей повседневной эксплуатации. \n  Только в сочетании красоты и удобства, дизайн будет уникальным и потрясающим. \n  А дом, в котором вы будите проводить время  комфортным и уютным.'
    },
    {
        id: 5,
        title: 'Внутренняя отделка',
        active: false,
        text: '   Обеспечим идеальное качество отделки дома в полном соответствии с дизайн проектом. \n Произведем  монтаж  всех необходимых коммуникаций и ремонтные работы в черновой и чистовой отделке. \n Установим декор и завезем мебель. После завершения работ Вам останется только въехать в готовый дом.'
    },
])

const activedTab = computed(() => {
    let item = tabsList.value.filter(item => item.active == true)[0]
    return {
        title: item.title,
        text: item.text
    }
});

const disactiveTab = () => {
    tabsList.value.map(item => item.active = false)
}

const changeTab = (id) => {
    disactiveTab()
    tabsList.value.filter(item => item.id == id)[0].active = true
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.service {
    background-color: $gray;
    padding: 60px 0;

    &-title {
        color: rgba(167, 139, 115, 0.10);
        text-align: left;
        font-family: 'Inter';
        font-size: 70px;
        font-weight: 700;
        text-transform: uppercase;
    }

    &-subtitle {
        color: $primary-white;
        font-family: 'Inter';
        font-size: 48px;
        font-weight: 400;
        line-height: 56px;
        margin-top: -35px;
    }

    &-content {
        margin-top: 48px;
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        width: 100%;
    }

    &-text {
        color: $primary-white;
        font-family: 'Montserrat';
        font-size: 24px;
        font-weight: 400;
        line-height: 32px;
        max-width: 520px;
    }

    &-left {
        max-width: 550px;
        width: 100%;
    }

    &-right {
        max-width: 630px;
        width: 100%;
    }

    &__tabs {
        display: flex;
        flex-direction: column;
        gap: 48px;
        margin-top: 48px;

        &-item {
            display: flex;
            align-items: center;
            gap: 24px;
            cursor: pointer;
        }

        &-img {
            width: 35px;
            transition: .3s all;

            &.active {
                width: 50px;
            }

            img {
                width: 100%;
                object-fit: contain;
            }
        }

        &-title {
            color: $primary-white;
            font-family: 'Inter';
            font-size: 32px;
            font-weight: 400;
            line-height: 40px;
            transition: .3s all;

            &.active {
                font-weight: 600;
            }
        }
    }

    &__about {
        &-title {
            text-align: center;
            color: $white;
            font-family: 'Inter';
            font-size: 32px;
            font-weight: 400;
            height: 64px;
            display: flex;
            justify-content: center;
            align-items: end;
        }

        &-text {
            margin-top: 48px;
            color: $primary-white;
            text-align: justify;
            font-family: 'Montserrat';
            font-size: 24px;
            line-height: 32px;
            white-space: pre-wrap;
        }
    }
}
</style>