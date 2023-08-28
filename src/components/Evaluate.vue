<template>
  <article class="flex flex-col items-center justify-center w-full h-screen">
    <h3 class="text-3xl tracking-widest">顧客回饋</h3>
    <swiper
      :modules="modules"
      :pagination="{ clickable: true }"
      :slides-per-view="3"
      :space-between="40"
      :autoplay="{ delay: 8000 }"
      loop
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      class="w-[1024px] h-2/3 px-10"
    >
      <template v-for="item in data"
        ><swiper-slide
          ><div
            class="w-[300px] h-[400px] rounded-[24px] border border-solid border-slate-200 p-4 hover:shadow-lg hover:-translate-y-6 transition duration-300 ease-in-out cursor-pointer"
          >
            <div class="grid w-full h-full grid-rows-4 place-items-center">
              <div class="row-span-2 text-center">
                <h4 class="text-xl font-semibold">{{ item.title }}</h4>
                <p class="text-slate-400">
                  {{ item.content }}
                </p>
              </div>
              <div class="row-span-1">
                <div
                  class="bg-black h-[80px] w-[80px] rounded-full mt-14 overflow-hidden"
                >
                  <img
                    :src="item.imgUrl"
                    class="w-full h-full"
                    :alt="item.customName + '的照片'"
                  />
                </div>
              </div>
              <div class="row-span-1">{{ item.customName }}</div>
            </div>
          </div></swiper-slide
        ></template
      >
    </swiper>
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

const data = ref([
  {
    title: "獨特創意",
    content:
      "他們家的甜點就像是治癒系神器，每一口都讓我感覺活過來，就像貓咪又恢復了九條命！",
    imgUrl: "src/assets/img/custom/1_0007.jpg",
    customName: "台北房東",
  },
  {
    title: "美味",
    content:
      "這家甜點店就像是走進了甜點的神秘森林，味道就像用了魔法一樣，讓我逃不出這個美味陷阱！",
    imgUrl: "src/assets/img/custom/1_0005.jpg",
    customName: "小當家",
  },
  {
    title: "多元選擇",
    content:
      "超級愛他們家的甜點！每次光顧都能品嚐到新驚喜，簡直是我的甜蜜後援。",
    imgUrl: "src/assets/img/custom/1_0006.jpg",
    customName: "早餐店阿姨",
  },
  {
    title: "客製化服務",
    content:
      "老闆真是創意無限，每款點心都是驚艷的藝術品，絕對是味蕾的震撼之旅。",
    imgUrl: "src/assets/img/custom/1_0004.jpg",
    customName: "會說話的鵝",
  },
  {
    title: "良好服務",
    content:
      "這裡的服務真的超級貼心，每一次光顧都讓我有回家的感覺，真的很窩心。",
    imgUrl: "src/assets/img/custom/1_0003.jpg",
    customName: "山道猴子",
  },
  {
    title: "季節驚喜",
    content:
      "不論是甜點的味道還是外觀，這家店總能給我驚喜，讓我對甜品有了新的認識。",
    imgUrl: "src/assets/img/custom/1_0002.jpg",
    customName: "兔田佩口拉",
  },
  {
    title: "無限創新",
    content:
      "每次光顧都能發現新甜點，我跟他們家的甜點，簡直是無法自拔的互迷關係！",
    imgUrl: "src/assets/img/custom/1_0001.jpg",
    customName: "五條悟",
  },
]);

const onSwiper = (swiper: SwiperRef) => {
  console.log(swiper);
};
const onSlideChange = (e: SwiperRef) => {
  console.log("slide change", e.activeIndex);
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