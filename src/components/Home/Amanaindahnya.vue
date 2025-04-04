<script setup lang="ts">
import Image from "../../assets/Home/AmanaIndahmua/Frame 1707481762.png";
import Facebook from "../../assets/icons/facebook.svg";
import Insta from "../../assets/icons/insta.svg";
import Twitter from "../../assets/icons/Twitter.svg";
</script>

<template>
  <section class="bg-[#F9F5F4] mt-5">
    <div
      class="container flex flex-col md:flex-row gap-8 md:gap-0 items-center"
    >
      <div class="flex-1">
        <img class="w-[100%] h-[100%] object-cover" :src="Image" alt="" />
      </div>
      <div class="flex-1 px-10">
        <h1
          class="text-[33px] sm:text-[40px] text-[#2D3B3B] md:text-[48px] lg:text-[54px] leading-[120%] uppercase font-newYork pb-3 lg:pb-10"
        >
          AMANA INDAHNYA
        </h1>
        <p
          class="text-[16px] md:text-[18px] lg:text-[22px] text-[#2D3B3BE5] leading-[180%] lg:leading-[200%]"
        >
          This photography website is a true gem for anyone who appreciates
          artistry and storytelling through the lens. The images are
          awe-inspiring, and the website provides an engaging and immersive
          experience. With a few minor enhancements in user-friendliness and
          performance, it could become an even more exceptional platform for
          showcasing photography talent.
        </p>
        <div class="flex gap-4 py-3">
          <img class="w-[50px]" :src="Facebook" alt="" />
          <img class="w-[50px]" :src="Insta" alt="" />
          <img class="w-[50px]" :src="Twitter" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>
