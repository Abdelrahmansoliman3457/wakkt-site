<template>
  <!-- start section info about us -->
  <div class="about-us relative-parent" id="about">
    <div class="container">
      <div class="item1-animation">
        <font-awesome-icon :icon="['fas', 'chart-line']" />
      </div>
      <div class="item2-animation">
        <font-awesome-icon :icon="['fas', 'arrows-turn-right']" />
      </div>
      <div class="item3-animation">
        <font-awesome-icon :icon="['fas', 'circle-dot']" />
      </div>
    </div>
    <div class="container">
      <h2 class="text-center mb-3">{{ $t("common.bestChoice") }}</h2>
      <p class="text-center limitid-p">
        {{ $t("nav.lorem") }}
      </p>
      <div class="row mt-5">
        <div class="col-md-6 mb-3">
          <div class="choice-row mb-4">
            <div class="big-dot bg-black"></div>
            <div class="left-text">
              <h5>{{ $t("common.wellIntegrated") }}</h5>
              <p>{{ $t("common.smallLorem") }}</p>
            </div>
          </div>
          <div class="choice-row mb-4">
            <div class="big-dot bg-gary"></div>
            <div class="left-text">
              <h5>{{ $t("common.wellIntegrated") }}</h5>
              <p>{{ $t("common.smallLorem") }}</p>
            </div>
          </div>
          <div class="choice-row mb-4">
            <div class="big-dot bg-light-gary"></div>
            <div class="left-text">
              <h5>{{ $t("common.wellIntegrated") }}</h5>
              <p>{{ $t("common.smallLorem") }}</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-12">
          <div class="app-phone2">
            <div class="imgs-container">
              <img
                :src="require('../assets/imgs/Minor Layer.png')"
                class="back-ground-phone"
                alt=""
              />

              <img
                :src="require('../assets/imgs/upper.png')"
                class="upper-phone"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- end section info about us -->
  <div class="statistics section-pad">
    <div class="container">
      <h2 class="mb-5">{{ $t("common.statistics") }}</h2>
      <div class="row mb-4">
        <div class="col-lg-3 col-md-4 col-12 mb-3">
          <div class="stats-box text-center">
            <img
              class="sm-img mb-2"
              :src="require('../assets/imgs/image 1.png')"
              alt=""
            />
            <div class="num-main mb-2">+30 k</div>
            <div class="stat-text">{{ $t("common.activeInst") }}</div>
          </div>
        </div>
        <div class="col-lg-3 col-md-4 col-12 mb-3">
          <div class="stats-box text-center">
            <img
              class="sm-img mb-2"
              :src="require('../assets/imgs/image 2.png')"
              alt=""
            />
            <div class="num-main mb-2">+40</div>
            <div class="stat-text">{{ $t("common.awards") }}</div>
          </div>
        </div>
        <div class="col-lg-3 col-md-4 col-12 mb-3">
          <div class="stats-box text-center">
            <img
              class="sm-img mb-2"
              :src="require('../assets/imgs/image 3.png')"
              alt=""
            />
            <div class="num-main mb-2">+30 k</div>
            <div class="stat-text">{{ $t("common.happyClients") }}</div>
          </div>
        </div>
        <div class="col-lg-3 col-md-4 col-12 mb-3">
          <div class="stats-box text-center">
            <img
              class="sm-img mb-2"
              :src="require('../assets/imgs/image 4.png')"
              alt=""
            />
            <div class="num-main mb-2">+500 k</div>
            <div class="stat-text">{{ $t("common.rates") }}</div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-7 col-12 mb-3">
          <div class="stats-img-cont">
            <img
              :src="require('../assets/imgs/Rectangle 2924464.png')"
              alt=""
            />
            <a href="#" class="vedio-open">
              <i class="fa-solid fa-play"></i>
            </a>
          </div>
        </div>
        <div class="col-md-5 col-12">
          <div class="slider-mini">
            <swiper
              :pagination="pagination"
              :modules="modules"
              :navigation="true"
              class="mySwiper"
              :autoplay="{
                delay: 3500,
                disableOnInteraction: false,
              }"
              :loop="true"
            >
              <swiper-slide
                class="home-item"
                v-for="slider in sliders"
                :key="slider"
              >
                <img class="home-img" :src="slider.src" alt="" />
              </swiper-slide>
            </swiper>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
// import required modules
import { Autoplay, Pagination } from "swiper";
export default {
  data() {
    return {
      sliders: [
        {
          src: require("../assets/imgs/Rectangle 2924464.png"),
        },
        {
          src: require("../assets/imgs/Rectangle 2924464.png"),
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
      pagination: {
        clickable: true,
      },

      modules: [Pagination, Autoplay],
    };
  },
};
</script>

<style>
.slider-mini .swiper-slide {
  height: 350px;
}
.slider-mini img {
  width: 100%;
  height: 100%;
}
</style>
