<template>
    <section class="answers">
        <div class="container">
            <h2 class="answers-title">
                Часто задаваемые вопросы
            </h2>
            <div
                id="questions"
                class="questions"
            >
                <div class="accordion">
                    <div
                        v-for="(item, index) in accordion"
                        :key="index"
                        class="accordion__section"
                    >
                        <button
                            class="accordion__header"
                            @click="isOpenAccordion(item)"
                        >
                            <h1 class="accordion-title">{{ item.title }}</h1>
                            <div class="accordion-arrow">
                                <img
                                    :class="item.active ? 'accordion-arrow__open' : 'accordion-arrow__close'"
                                    :src="akkordionImg"
                                    alt="arrow"
                                >
                            </div>
                        </button>
                        <div
                            :ref="'accordion' + item.id"
                            class="accordion__content"
                            :class="{ active: item.active }"
                        >
                            <p>
                                {{ item.text }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import akkordionImg from '../assets/images/svg/select-open.svg';

import { ref } from 'vue'

const accordion = ref([
    {
        id: 1,
        title: 'Сколько стоит строительство?',
        text: 'Много ого ipsam itaque expedita. Assumenda labore inventore, quod id eos culpa iure, molestiae ration vero fugiat nulla aspernatur harum unde deleniti quia eum rerum? Obcaecati in itaque dicta iste  amet quae repudiandae, cum cupiditate laudantium quasi quis soluta eius autem nihil explicipsam itaque expedita. Assumenda labore inventore, quod id eos culpa iure, molestiae ration vero fugiat nulla aspernatur harum unde deleniti quia eum rerum? Obcaecati in itaque dicta iste  amet quae repudiandae, cum cupiditate laudantium quasi quis soluta eius autem nihil explicabo',
        active: false,
    },
    {
        id: 2,
        title: 'Зачем нужен проект дома?',
        text: 'Много',
        active: false,
    },
    {
        id: 3,
        title: 'Для чего нужна геология участка?',
        text: 'Много',
        active: false,
    },
    {
        id: 4,
        title: 'Из чего строить дом?',
        text: 'Много',
        active: false,
    },
    {
        id: 5,
        title: 'Вы можете провести экспертизу проекта?',
        text: 'Много',
        active: false,
    },
    {
        id: 6,
        title: 'Сколько стоит индивидуальное проектирование?',
        text: 'Много',
        active: false,
    },
])


const isOpenAccordion = (item) => {
    item.active = !item.active;

    const accordionBody = document.querySelectorAll('.accordion__content');
    let id = item.id - 1

    accordionBody[id].classList.toggle('active');
    if (item.active) {
        accordionBody[id].style.maxHeight = accordionBody[id].scrollHeight + 'px';
    } else {
        accordionBody[id].style.maxHeight = '0';
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.answers {
    padding: 120px 0 80px;

    &-title {
        color: $gray;
        font-family: 'Inter';
        font-size: 48px;
        font-weight: 400;
        line-height: 56px;
    }
}

.accordion {
    margin-top: 15px;
    display: flex;
    flex-direction: column;
    gap: 8px;
    width: 100%;

    // accordion header
    &__header {
        padding: 24px 0;
        display: flex;
        align-items: center;
        gap: 10px;
        justify-content: space-between;
        width: 100%;
        border-bottom: 1px solid $gray;
    }

    &-title {
        color: $black;
        font-family: 'Inter';
        font-size: 32px;
        font-weight: 400;
        line-height: 40px;
    }

    &-arrow {
        width: 30px;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;

        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        &__open {
            transform: rotate(180deg);
            transition: .3s;
        }

        &__close {
            transform: rotate(0deg);
            transition: .3s;
        }
    }

    &__content {
        opacity: 0;
        visibility: hidden;
        height: auto;
        // min-height: 0;
        max-height: 0;
        transition: max-height .4s, visibility .3s, opacity .3s;

        p {
            padding: 20px 16px;
            color: $black;
            font-family: 'Inter';
            font-size: 20px;
            font-weight: 400;
            line-height: 26px;
        }

        &.active {
            opacity: 1;
            visibility: visible;
            transition: max-height .4s, visibility .5s, opacity .6s;
        }
    }


}
</style>