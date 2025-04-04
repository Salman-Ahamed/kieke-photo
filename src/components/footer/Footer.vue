<script setup lang="ts">
import Logo2 from "../../assets/Home/logo2.png";
import RoundArrow from "../../assets/Home/roundArrow.png";
import { navItems } from "../../data/data.ts";
</script>

<template>
  <footer class="bg-[#2D3B3B] pt-10 pb-2">
    <div class="container px-2">
      <div class="flex flex-col items-center justify-center">
        <div class="relative flex flex-col items-center space-y-5">
          <img :src="Logo2" alt="" />
          <div class="absolute top-0 right-0 w-[60px] h-[60px]">
            <img :src="RoundArrow" alt="" class="w-full h-full" />
          </div>
          <p
            class="text-[14px] md:text-[16px] lg:text-[18px] leading-[180%] text-center md:px-20 text-[#FFFFFFE5] font-helvatika"
          >
            This photography website is a true gem for anyone who appreciates
            artistry and storytelling through the lens. The images are
            awe-inspiring, and the website provides an engaging and immersive
            experience. With a few minor enhancements in user-friendliness and
            performance, it could become an even more exceptional platform for
            showcasing photography talent.
          </p>
        </div>
        <!-- navItems  -->
        <div
          class="flex border-b border-gray-500 w-full py-10 gap-5 text-[#FFFFFF] text-[14px] md:text-[16px] leading-[16px] items-center justify-center flex-wrap"
        >
          <a href="#" v-for="(item, index) in navItems">{{ item.name }}</a>
        </div>
        <!-- ---------------- -->
        <div
          class="flex justify-between w-full py-5 text-[#FFFFFF] items-center"
        >
          <div class="space-y-2">
            <p class="text-[14px] md:text-[16px] leading-[120%]">
              All rights reserved
            </p>
            <p class="text-[14px] md:text-[16px] leading-[120%]">
              @2025KIEKEFOTOGRAGIE
            </p>
          </div>
          <div class="space-y-2">
            <p class="text-[14px] md:text-[16px] leading-[120%]">
              TERMS & CONDITIONS
            </p>
            <p class="text-[14px] md:text-[16px] leading-[120%]">
              PRIVACY POLICY
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
