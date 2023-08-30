<script setup lang="ts">
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Nav from "./components/Nav.vue";
import Baker from "./components/Baker.vue";
import ReturnTop from "./components/ReturnTop.vue";
import Evaluate from "./components/Evaluate.vue";
import Footer from "./components/Footer.vue";
import Announcement from "./components/Announcement.vue";
import Banner from "./components/Banner.vue";
</script>

<template>
  <div class="relative">
    <Header class="absolute" />
    <Nav class="absolute top-[80px]" />
    <Main class="absolute" />
    <Announcement />
    <Banner />

    <Baker />

    <Evaluate />
    <ReturnTop class="z-50" />
    <Footer />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
