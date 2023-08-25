<script setup lang="ts">
import Header from "./components/Header.vue";

import Nav from "./components/Nav.vue";
import Baker from "./components/Baker.vue";
import ReturnTop from "./components/ReturnTop.vue";
import Evaluate from "./components/Evaluate.vue";
</script>

<template>
  <Header class="absolute" />
  <Nav class="sticky top-0 -mt-[863px]" />
  <div class="mt-[863px]">
    <Baker />
    <Evaluate />
  </div>
  <ReturnTop class="z-50" />
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
