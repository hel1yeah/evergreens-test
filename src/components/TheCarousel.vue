<template>
  <div class="carousel__wrapper">
    <Carousel :settings="settings">
      <Slide v-for="slide in slides" :key="slide">
        <div class="carousel__item">
          <img class="carousel__item-img" :src="slide" alt="slide" />
        </div>
      </Slide>
    </Carousel>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "TheCarousel",
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      slides: [
        require("../assets/images/slide1.png"),
        require("../assets/images/slide1.png"),
        require("../assets/images/slide1.png"),
        require("../assets/images/slide1.png"),
      ],
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
        autoplay: "7000",
        wrapAround: true,
        transition: "2000",
        mouseDrag: false,
      },
    };
  },
});
</script>

<style>
.carousel__wrapper {
  position: absolute;
  display: block;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: -1;
}
.carousel__item {
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.carousel__item-img {
  height: 100%;
}
</style>
