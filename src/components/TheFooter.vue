<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer__logo">
                    <a
                        href="#"
                        class="footer__logo-img"
                    >
                        <img
                            :src="footerLogo"
                            alt="footer logo"
                        >
                    </a>
                    <h4 class="footer__logo-text">Архитектурно-строительная группа</h4>
                </div>
                <nav class="footer-nav">
                    <ul class="nav__list">
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                Проектирование
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                Каталог проектов
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                Контакты
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                Строительство
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                О компании
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                href="#"
                                class="nav__list-link"
                            >
                                Полезные статьи
                            </a>
                        </li>
                    </ul>
                </nav>
                <div class="footer-info">
                    <a
                        href="tel:+"
                        class="footer-call"
                    >+7 (495) 799-75-29
                    </a>
                    <div class="footer-schedule">
                        Рабочее время:
                        <span> Ежедневно 10:00 - 21:00</span>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <a
                    href="№"
                    class="footer-terms"
                >
                    Политика конфиденциальности</a>
                <div class="footer-copyright">
                    Архитектурно-строительная группа ARHION © 2001 - 2023
                </div>
                <ul class="social__list">
                    <li class="social__list-item">
                        <a
                            class="social__list-link"
                            href="#"
                        >
                            <img
                                :src="vkLogo"
                                alt="vk logo"
                            >
                        </a>
                    </li>
                    <li class="social__list-item">
                        <a
                            class="social__list-link"
                            href="#"
                        >
                            <img
                                :src="instaLogo"
                                alt="insta logo"
                            >
                        </a>
                    </li>
                    <li class="social__list-item">
                        <a
                            class="social__list-link"
                            href="#"
                        >
                            <img
                                :src="whatsupLogo"
                                alt="whatsup logo"
                            >
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script setup>
import footerLogo from '../assets/images/svg/footer-logo.svg'
import instaLogo from '../assets/images/svg/instagram.svg'
import vkLogo from '../assets/images/svg/vk.svg'
import whatsupLogo from '../assets/images/svg/whatsapp.svg'
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.footer {
    padding: 60px 0 40px;
    color: $primary-white;
    background-color: $gray;

    &-content {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
    }

    &__logo {
        display: flex;
        flex-direction: column;
        gap: 16px;
        align-items: flex-start;
        max-width: 230px;

        &-img {
            display: inline-block;
            width: 67px;
            height: 70px;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }

        &-text {
            font-family: 'Montserrat';
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
        }
    }

    &-info {
        display: flex;
        flex-direction: column;
        gap: 14px;
        max-width: 160px;
    }

    &-call {
        font-family: 'Inter';
        font-size: 16px;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0.16px;
    }

    &-schedule {
        font-family: 'Inter';
        font-size: 13px;
        font-style: normal;
        font-weight: 400;
        line-height: 22px;

        span {
            display: block;
        }
    }

    &-bottom {
        margin-top: 30px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &-terms {
        font-family: 'Montserrat';
        font-size: 12px;
        font-weight: 400;
        line-height: 16px;
        border-bottom: 1px solid $primary-white;
    }

    &-copyright {
        font-family: 'Montserrat';
        font-size: 16px;
        font-weight: 400;
        line-height: 24px;
    }
}

.nav {
    &__list {
        display: flex;
        flex-wrap: wrap;
        column-gap: 70px;
        row-gap: 32px;
        max-width: 590px;
        width: 100%;

        &-link {
            display: inline-block;
            font-family: 'Montserrat';
            font-size: 16px;
            font-weight: 400;
            line-height: 24px;
            width: 150px;
        }
    }
}

.social__list {
    display: flex;
    gap: 16px;
    align-items: center;

    &-link {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 36px;
        height: 36px;
        background-color: $gold;
        border-radius: 50%;

        img {
            width: 20px;
            height: 20px;
            object-fit: contain;
        }
    }
}
</style>