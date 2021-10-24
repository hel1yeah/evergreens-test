<template>
  <section class="wrapper">
    <vue-carousel></vue-carousel>
    <app-header></app-header>
  </section>
  <main></main>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import VueCarousel from "./components/VueCarousel.vue";

export default {
  components: {
    AppHeader,
    VueCarousel,
  },
  name: "App",
};
</script>

<style lang="scss">
.wrapper {
  position: relative;
}
</style>
