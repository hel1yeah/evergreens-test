<template>
  <section class="wrapper-header">
    <the-carousel></the-carousel>
    <the-header></the-header>
    <the-nav></the-nav>
  </section>
  <main class="main">
    <div class="container">
      <div class="main__wrapper">
        <the-descr></the-descr>
      </div>
    </div>
  </main>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheCarousel from "./components/TheCarousel.vue";
import TheNav from "./components/TheNav.vue";
import TheDescr from "./components/TheDescr.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    TheCarousel,
    TheNav,
    TheDescr,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/_mixin.scss";
.wrapper-header {
  position: relative;
}

.main {
}
.main__wrapper {
  @include myFlex;
}
</style>
