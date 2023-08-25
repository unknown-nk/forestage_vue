<template>
  <article class="relative w-full h-screen bg-slate-400">
    <div class="absolute z-40 right-[10%] top-[50%] text-white">
      <h2 class="text-3xl">今天吃了沒?</h2>
      <button
        class="w-[200px] h-[50px] bg-yellow-500 hover:bg-yellow-700 font-bold py-2 px-4 rounded"
      >
        快速訂購
      </button>
    </div>
    <div class="absolute z-30 w-full h-full bg-black opacity-50"></div>
    <video
      autoplay
      muted
      loop
      class="absolute top-0 object-cover w-full h-full"
    >
      <source
        src="https://cdn.coverr.co/videos/coverr-decorating-a-cake-9004/1080p.mp4"
        type="video/mp4"
      />
    </video>
  </article>
</template>

<script setup lang="ts">
</script>

<style lang="scss" scoped>
</style>
