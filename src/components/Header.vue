<template>
  <header class="w-full h-[80px] z-40 grid grid-cols-4 text-white">
    <h1 class="col-span-1 z-50">
      <p
        class="h-full pl-[90px] text-lg font-bold leading-normal flex items-center"
      >
        Dessert Town
      </p>
    </h1>
    <div class="col-start-3 col-span-2 z-50 place-self-end self-center">
      <ul class="flex">
        <li class="px-2"><i></i>會員登入</li>
        <li class="px-2"><i></i>關於我們</li>
      </ul>
    </div>
    <div class="w-full h-full bg-black opacity-60 absolute"></div>
  </header>
</template>
<script setup lang="ts">
</script>
<style lang="scss" scoped>
h1 {
  background-image: url('../assets/img/logo.svg');
  background-size: 120%;
  background-position-y: center;
  width: 80px;
  height: 80px;
}
</style>