<script setup>
import { onMounted } from "vue";

import SmoothScroll from "smoothscroll-for-websites";

onMounted(() => {
  SmoothScroll({
    animationTime: 500,
    stepSize: 60,
    keyboardSupport: true,
    arrowScroll: 100,
    touchpadSupport: true,
  });
});
</script>

<template>
  <RouterView />
</template>

<style lang="scss"></style>
