<template>
    <header class="header">
        <div class="container">
            <div class="header-logo">
                <img
                    :src="logo"
                    alt="logo"
                >
            </div>
            <div class="header-content">
                <div class="header-contact">
                    +7 (495) 799-75-29 | Ежедневно 10:00-21:00
                </div>
                <nav class="nav">
                    <ul class="nav__list">
                        <li class="nav__list-item">
                            <a
                                class="nav__list-link"
                                href="#"
                            >
                                <img
                                    :src="whatsUpIcon"
                                    alt="user icon"
                                >
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                class="nav__list-link"
                                href="#"
                            >
                                <img
                                    :src="telegramIcon"
                                    alt="user icon"
                                >
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <a
                                class="nav__list-link nav__list-profile"
                                href="#"
                            >
                                <img
                                    :src="userIcon"
                                    alt="user icon"
                                >
                            </a>
                        </li>
                        <li class="nav__list-item">
                            <div class="nav__open">
                                <div class="nav__open-btn">
                                    <div class="btn-elem"></div>
                                </div>
                            </div>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>

    </header>
</template>

<script setup>
import logo from '../assets/logo.svg'
import userIcon from '../assets/images/svg/user.svg'
import whatsUpIcon from '../assets/images/svg/whatsup.svg'
import telegramIcon from '../assets/images/svg/telegram.svg'
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.header {
    padding: 15px 0 12px;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &-logo {
        width: 290px;
        height: 56px;

        img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    &-content {
        display: flex;
        align-items: center;
        gap: 100px;
    }

    &-contact {
        color: $black;
        font-family: 'Montserrat';
        font-size: 20px;
        font-weight: 400;
        line-height: 28px;
    }
}


.nav {
    &__list {
        display: flex;
        align-items: center;
        gap: 24px;

        &-item {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 32px;
            height: 32px;
        }

        &-link {
            width: 100%;
            height: 100%;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }

        &-profile {
            width: 46px;
            height: 46px;
            margin-left: -14px;
            margin-right: -14px;
        }
    }

    &__open {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 32px;
        height: 32px;
        cursor: pointer;

        &-btn {
            display: flex;
            align-items: center;
            justify-content: center;

            .btn-elem {
                position: relative;
                width: 30px;
                height: 3px;
                border-radius: 10px;
                background: $black;

                &::before {
                    position: absolute;
                    content: "";
                    display: block;
                    width: 30px;
                    height: 3px;
                    border-radius: 10px;
                    top: -10px;
                    background: $black;
                }

                &::after {
                    position: absolute;
                    content: "";
                    display: block;
                    width: 30px;
                    height: 3px;
                    border-radius: 10px;
                    top: 10px;
                    background: $black;
                }
            }
        }
    }

    // &__exit {
    //     display: none;
    //     justify-content: center;
    //     align-items: center;
    //     width: 40px;
    //     height: 40px;
    //     cursor: pointer;
    //     position: absolute;
    //     right: 10px;
    //     top: 20px;

    //     @media (max-width: 768px) {
    //         display: flex;
    //     }

    //     &-btn {
    //         display: flex;
    //         align-items: center;
    //         justify-content: center;

    //         .btn-elem {
    //             position: relative;
    //             width: 30px;
    //             height: 2.5px;
    //             border-radius: 10px;
    //             background: transparent;

    //             &::before {
    //                 position: absolute;
    //                 content: "";
    //                 display: block;
    //                 width: 30px;
    //                 height: 2.5px;
    //                 border-radius: 10px;
    //                 transform: rotate(45deg);
    //                 top: 0;
    //                 background: white;
    //             }

    //             &::after {
    //                 position: absolute;
    //                 content: "";
    //                 display: block;
    //                 width: 30px;
    //                 height: 2.5px;
    //                 border-radius: 10px;
    //                 background: white;
    //                 transform: rotate(-45deg);
    //                 top: 0;
    //             }
    //         }
    //     }
    // }
}
</style>