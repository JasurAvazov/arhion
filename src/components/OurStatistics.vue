<template>
    <div class="statistics">
        <div class="container">
            <div class="statistics__item">
                <h3 class="statistics__item-title">2K+</h3>
                <h4 class="statistics__item-text">СДАННЫХ ПРОЕКТОВ</h4>
            </div>
            <div class="statistics__item">
                <h3 class="statistics__item-title">20+</h3>
                <h4 class="statistics__item-text">КОМАНД</h4>
            </div>
            <div class="statistics__item">
                <h3 class="statistics__item-title">2,5K+</h3>
                <h4 class="statistics__item-text">КЛИЕНТОВ</h4>
            </div>
        </div>
    </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.statistics {
    background: rgba(241, 235, 230, 0.72);
    padding: 60px 0;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
    }

    &__item {
        display: flex;
        flex-direction: column;
        gap: 18px;
        align-items: center;
        width: calc(100%/3 - 15px);

        &-title {
            color: $gray-light;
            text-align: center;
            font-family: 'Inter';
            font-size: 80px;
            font-weight: 400;
        }

        &-text {
            color: $gray;
            text-align: center;
            font-family: 'Montserrat';
            font-size: 34px;
            font-weight: 400;
            letter-spacing: 15px;
        }
    }
}
</style>