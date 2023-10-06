<template>
    <section class="advice">
        <div class="container">
            <div class="advice-wrapper">
                <h2 class="advice-title">Нужна консультация?</h2>
                <h3 class="advice-subtitle">Оставьте контакты и мы с вами свяжемся для обсуждения деталей</h3>
                <div class="advice-content">
                    <ul class="advice__contacts">
                        <li class="advice__contacts-item">
                            <a
                                href="#"
                                class="advice__contacts-link"
                            >
                                <div class="advice__contacts-img">
                                    <img
                                        :src="whatsUpIcon"
                                        alt="what's up icon"
                                    >
                                </div>
                                <div class="advice__contacts-title social-title">WHATSAPP
                                    <span>
                                        <img
                                            :src="btnArrowIcon"
                                            alt="btn arrow"
                                        >
                                    </span>
                                </div>
                            </a>
                        </li>
                        <li class="advice__contacts-item">
                            <a
                                href="#"
                                class="advice__contacts-link"
                            >
                                <div class="advice__contacts-img">
                                    <img
                                        :src="telegramIcon"
                                        alt="what's up icon"
                                    >
                                </div>
                                <div class="advice__contacts-title social-title">TELEGRAM
                                    <span>
                                        <img
                                            :src="btnArrowIcon"
                                            alt="btn arrow"
                                        >
                                    </span>
                                </div>
                            </a>
                        </li>
                        <li class="advice__contacts-item">
                            <a
                                href="#"
                                class="advice__contacts-link"
                            >
                                <div class="advice__contacts-img">
                                    <img
                                        :src="phoneIcon"
                                        alt="what's up icon"
                                    >
                                </div>
                                <div class="advice__contacts-title">+7 (495) 799-75-29</div>
                            </a>
                        </li>
                    </ul>
                    <form class="form">
                        <input
                            class="form-input"
                            name="name"
                            placeholder="Имя"
                            type="text"
                            id="name"
                        >
                        <input
                            class="form-input"
                            type="number"
                            placeholder="Телефон"
                            name="phone"
                            id="phone"
                        >
                        <button class="form-btn">
                            <div>
                                Отправить
                                <span>
                                    <img
                                        :src="btnArrowIcon"
                                        alt="btn arrow"
                                    >
                                </span>
                            </div>
                        </button>
                    </form>
                </div>
            </div>
            <div class="advice__banner">
                <div class="advice__banner-img">
                    <img
                        :src="reviewImg"
                        alt="image advice"
                    >
                </div>
                <p class="advice__banner-text">
                    Строим, проектируем и наполняем смыслами
                </p>
            </div>
        </div>
    </section>
</template>

<script setup>
import whatsUpIcon from '../assets/images/svg/whatsup.svg';
import telegramIcon from '../assets/images/svg/telegram.svg';
import phoneIcon from '../assets/images/svg/phone.svg';
import btnArrowIcon from '../assets/images/svg/btn-arrow.svg';
import reviewImg from '../assets/images/png/reviewLogo.png';

</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.advice {
    background: #F1EBE6;
    padding: 70px 0 80px;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &-title {
        color: $gray;
        font-family: 'Inter';
        font-size: 48px;
        font-weight: 400;
        line-height: 48px;
    }

    &-subtitle {
        margin-top: 40px;
        color: $gray;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 400;
    }

    &-content {
        margin-top: 40px;
        display: flex;
        align-items: flex-start;
        gap: 60px;
    }

    &__contacts {
        display: flex;
        gap: 24px;
        flex-direction: column;

        &-item {
            padding: 11px 0 0;
        }

        &-link {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        &-img {
            width: 30px;
            height: 30px;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }

        &-title {
            color: $gray;
            font-family: 'Montserrat';
            font-size: 20px;
            font-weight: 400;
            line-height: 22px;
            display: flex;
            align-items: center;
            width: 230px;
            position: relative;

            &.social-title {
                border-bottom: 1px solid $gray;
            }

            span {
                position: absolute;
                right: -1px;
                top: -3px;
                width: 45px;
                height: 30px;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }
        }
    }

    &__banner {
        background-color: $gray;
        width: 550px;
        padding: 60px 20px;
        display: flex;
        flex-direction: column;
        gap: 25px;
        align-items: center;

        &-img {
            width: 85%;

            img {
                width: 100%;
            }
        }

        &-text {
            color: $primary-white;
            text-align: center;
            font-family: 'Inter';
            font-size: 28px;
            font-weight: 400;
            line-height: 40px;
            max-width: 380px;
        }
    }
}

.form {
    display: flex;
    flex-direction: column;
    gap: 24px;
    width: 360px;

    &-input {
        width: 100%;
        display: block;
        padding: 8px 0;
        font-family: 'Montserrat';
        font-size: 20px;
        color: $gray;
        font-weight: 400;
        line-height: 24px;
        outline: none;
        border: none;
        border-bottom: 1px solid $gray;
        background-color: transparent;

        &::placeholder {
            color: $gray-text;
        }
    }

    &-btn {
        padding: 11px 0;
        width: 270px;

        div {
            width: 100%;
            display: flex;
            align-items: center;
            position: relative;
            border-bottom: 1px solid $gray;

            span {
                position: absolute;
                right: -1px;
                top: -3px;
                width: 45px;
                height: 30px;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }
        }

        color: $gray;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 400;
        line-height: 22px;

    }
}
</style>