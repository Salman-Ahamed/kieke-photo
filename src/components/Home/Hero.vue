<script setup lang="ts">
import HeroImage from "../../assets/Home/heroImage.png";
</script>

<template>
  <section
    id="home"
    class="container px-2 pt-10 pb-5 flex flex-col md:flex-row gap-y-5 gap-2"
  >
    <div class="flex-1 flex flex-col items-start justify-center">
      <h1
        class="text-[48px] md:text-[68px] lg:text-[78px] font-newYork leading-[120%] text-[#2D3B3B]"
      >
        CAPTURING <span class="text-[#2D3B3BB2]">MOMENTS</span> IN
        <br class="hidden md:block" />
        TIME
      </h1>
      <p class="text-[#2D3B3BE5] py-4">
        A Glimpse Into the Past, a Snapshot of the Present.
      </p>
      <button
        class="bg-black mt-2 rounded-full px-4 py-2 text-white text-[16px]"
      >
        EXPLORE MORE
      </button>
    </div>
    <div class="flex-[1] max-h-[682px] overflow-hidden">
      <img class="size-full" :src="HeroImage" alt="" />
    </div>
  </section>
</template>
