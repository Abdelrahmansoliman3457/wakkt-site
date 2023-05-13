<template>
  <!--start section companies-->
  <div class="container">
    <div class="companies section-pad">
      <h2 class="text-center">
        {{ $t("common.join") }}
        <span class="color-main"> {{ $t("common.wakkt") }} </span>
      </h2>
      <div class="slider mt-4">
        <swiper
          :slidesPerView="7"
          :spaceBetween="100"
          :slidesPerGroup="1"
          :loop="true"
          class="mySwiper"
          :autoplay="{
            delay: 3500,
            disableOnInteraction: false,
          }"
          :modules="modules"
        >
          <swiper-slide v-for="cat in catsImages" :key="cat">
            <router-link :to="'/catogryView/' + cat.id" class="categories-item">
              <div class="img-style-con">
                <img class="cat-img" :src="cat.src" alt="" />
              </div>
            </router-link>
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </div>
  <!--end section companies-->
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";
import { Autoplay } from "swiper";
export default {
  data() {
    return {
      catsImages: [
        {
          id: 1,
          src: require("../assets/imgs/Group 97806.svg"),

        },
        {
          id: 2,
          src: require("../assets/imgs/Group 97806.svg"),
  
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 3,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
        {
          src: require("../assets/imgs/Group 97806.svg"),
          id: 4,
        },
       
   
      ],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay],
    };
  },
};
</script>

<style></style>
