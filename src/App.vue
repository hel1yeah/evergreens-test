<template>
  <section class="wrapper-header">
    <vue-carousel></vue-carousel>
    <app-header></app-header>
    <main class="main">
      <app-nav></app-nav>
    </main>
  </section>
  <main></main>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import VueCarousel from "./components/VueCarousel.vue";
import AppNav from "./components/AppNav.vue";

export default {
  components: {
    AppHeader,
    VueCarousel,
    AppNav,
  },
  name: "App",
};
</script>

<style lang="scss">
.wrapper-header {
  position: relative;
}
</style>
