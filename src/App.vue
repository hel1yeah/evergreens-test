<template>
  <section class="wrapper-header">
    <the-carousel></the-carousel>
    <the-header></the-header>
    <the-nav></the-nav>
  </section>
  <main class="main">
    <div class="main__wrapper"></div>
  </main>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheCarousel from "./components/TheCarousel.vue";
import TheNav from "./components/TheNav.vue";

export default {
  components: {
    TheHeader,
    TheCarousel,
    TheNav,
  },
  name: "App",
};
</script>

<style lang="scss">
.wrapper-header {
  position: relative;
}
</style>
