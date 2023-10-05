<template>
    <section class="banner">
        <div class="banner-img">
            <img
                :src="content.bgLink"
                alt="banner image"
            >
        </div>
        <div class="banner-title">
            {{ content.title }}
        </div>
    </section>
</template>

<script setup>
const { content } = defineProps(['content']);

</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.banner {
    background-color: $gold;
    display: flex;
    align-items: center;
    gap: 34px;
    max-width: 1920px;
    margin: auto;
    width: 100%;

    &-img {
        width: 500px;
        height: 310px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    &-title {
        color: $white;
        font-family: 'Inter';
        font-size: 46px;
        font-weight: 600;
        max-width: 800px;
    }
}
</style>