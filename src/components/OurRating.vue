<template>
    <section class="rating">
        <div class="container">
            <div class="rating__count">
                <h3 class="rating__count-num">300+</h3>
                <h4 class="rating__count-title">положительных оценок</h4>
            </div>
            <div class="rating__feedback">
                <div class="rating__feedback-images">
                    <img
                        :src="feedbackUserOne"
                        alt="feedback image"
                    >
                    <img
                        :src="feedbackUserTwo"
                        alt="feedback image"
                    >
                    <img
                        :src="feedbackUserThree"
                        alt="feedback image"
                    >
                    <img
                        :src="feedbackUserFour"
                        alt="feedback image"
                    >
                    <img
                        :src="feedbackUserFive"
                        alt="feedback image"
                    >
                </div>
                <h4 class="rating__feedback-title">сотни отзывов</h4>
            </div>
            <div class="rating__star">
                <div class="rating__star-list">
                    <img
                        :src="fullStar"
                        alt="star image"
                    >
                    <img
                        :src="fullStar"
                        alt="star image"
                    >
                    <img
                        :src="fullStar"
                        alt="star image"
                    >
                    <img
                        :src="fullStar"
                        alt="star image"
                    >
                    <img
                        :src="star"
                        alt="star image"
                    >
                </div>
                <h4 class="rating__star-title">рейтиннг 4.6
                    на Яндекс</h4>
            </div>
        </div>
    </section>
</template>

<script setup>
import feedbackUserOne from '../assets/images/png/feedbackOne.png'
import feedbackUserTwo from '../assets/images/png/feedbackTwo.png'
import feedbackUserThree from '../assets/images/png/feedbackThree.png'
import feedbackUserFour from '../assets/images/png/feedbackFour.png'
import feedbackUserFive from '../assets/images/png/feedbackFive.png'
import fullStar from '../assets/images/svg/star-full.svg'
import star from '../assets/images/svg/star.svg'

</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.rating {
    padding: 55px 0 60px;
    background: rgba(241, 235, 230, 0.72);

    .container {
        display: flex;
        align-items: flex-start;
        justify-content: space-between;

        h4 {
            color: $gray;
            text-align: center;
            font-family: 'Montserrat';
            font-size: 26px;
            font-weight: 400;
            letter-spacing: 11px;
        }
    }

    &__count {
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;

        &-num {
            color: $gray-light;
            text-align: center;
            font-family: 'Inter';
            font-size: 70px;
            font-weight: 400;
            line-height: 75px;
        }
    }

    &__feedback {
        display: flex;
        flex-direction: column;
        gap: 15px;
        align-items: center;

        &-images {
            display: flex;
            align-items: center;

            img {
                width: 95px;
                height: 96px;
                border-radius: 50%;
                object-fit: cover;

                &:not(:first-child) {
                    margin-left: -26px;
                }
            }
        }
    }

    &__star {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;

        &-list {
            display: flex;
            align-items: center;

            img {
                width: 75px;
                height: 75px;
                object-fit: contain;
            }
        }
    }
}
</style>