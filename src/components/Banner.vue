<template>
  <article class="w-full h-[40vh] relative overflow-hidden">
    <swiper
      :modules="modules"
      :pagination="{ clickable: true }"
      :slides-per-view="1"
      :space-between="40"
      :autoplay="{ delay: 8000 }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      class="w-[1024px] h-full px-10 absolute top-0 z-30"
    >
      <template v-for="items in bannerData">
        <swiper-slide>
          <div class="flex items-center">
            <img :src="items.bannerUrl" />
          </div>
        </swiper-slide>
      </template>
    </swiper>
    <div class="absolute -top-[50%] w-full h-full -z-10">
      <div class="flex items-center blur-md opacity-30">
        <img
          :src="bannerData[swiperIndex].bannerUrl"
          alt=""
          class="w-[200%] h-[200%]"
        />
      </div>
    </div>
  </article>
</template>
<script setup lang="ts">
/** import swiper */
import { ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, A11y, Autoplay } from "swiper/modules";
import { type Swiper as SwiperRef } from "swiper";
import "swiper/scss";
import "swiper/scss/pagination";

const bannerData = ref([
  {
    bannerUrl: "src/assets/img/banner/banner1.png",
  },
  {
    bannerUrl: "src/assets/img/banner/banner2.png",
  },
  {
    bannerUrl: "src/assets/img/banner/banner3.png",
  },
]);
const swiperIndex = ref(0);

const onSwiper = (swiper: SwiperRef) => {
  console.log(swiper);
};
const onSlideChange = (e: SwiperRef) => {
  console.log("slide change", e.activeIndex);
  swiperIndex.value = e.activeIndex;
  console.log(swiperIndex);
};
const modules = [Pagination, A11y, Autoplay];
</script>
<style lang="scss" scoped>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>