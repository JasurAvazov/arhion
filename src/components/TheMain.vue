<script setup>
import TheHeader from './TheHeader.vue';
import TheIntro from './TheIntro.vue';
</script>

<template>
    <div class="wrapper">
        <TheHeader></TheHeader>
        <TheIntro></TheIntro>
    </div>
</template>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

.wrapper {
    width: 100%;
    height: 90vh;
    background-image: url('../assets/images/jpg/intro.jpg');
    background-size: cover;
}
</style>