<script setup lang="ts">
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Nav from "./components/Nav.vue";
</script>

<template>
  <div class="relative">
    <Header class="absolute" />
    <Nav class="absolute top-[100px]" />
    <Main class="absolute" />
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
