<template>
  <div id="events" class="events-wrapper mt-[120px] mb-16">
    <Title class="text-center" >Мероприятия</Title>

    <div class="swiper-content">
        <swiper
          :modules="modules"
          :slides-per-view="3"
          :space-between="50"
          :breakpoints="breakPoints"
          :loop="true"
          :autoplay="true"
          navigation
        >
          <swiper-slide v-for="slide in slides" :key="slide.id" class="mt-12">
            <img :src="slide.img" alt="" class="mx-auto"/>
          </swiper-slide>
        </swiper>
    </div>
  </div>
</template>

<script>
import { Title } from "../ui-components";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, A11y, Autoplay } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/autoplay";
export default {
  components: {
    Title,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        { id: 1, img: "/assets/img/carusel1.png" },
        { id: 2, img: "/assets/img/carusel2.png" },
        { id: 3, img: "/assets/img/carusel3.png" },
        { id: 4, img: "/assets/img/carusel2.png" },
      ],
      breakPoints: {
        700:{ slidesPerView:3, },
        400:{ slidesPerView:2, }, 
        0:{ slidesPerView:1, }, 
      }
    };
  },
  setup() {
    return {
      modules: [Navigation, A11y, Autoplay],
    };
  },
};

</script>

<style>

.swiper-button-next, .swiper-button-prev{
  top: 7%;  
  transform: scale(0.7);
}
</style>