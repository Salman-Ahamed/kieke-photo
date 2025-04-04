<script setup lang="ts">
import i1 from "../../assets/Home/Afsched/i1.png";
import i2 from "../../assets/Home/Afsched/i2.png";
import i3 from "../../assets/Home/Afsched/i3.png";
import i4 from "../../assets/Home/Afsched/i4.png";
import i5 from "../../assets/Home/Afsched/i5.png";
import i6 from "../../assets/Home/Afsched/i6.png";
import i7 from "../../assets/Home/Afsched/i7.png";
</script>

<template>
  <section class="pt-4 md:pt-10 lg:pt-20 pb-5">
    <div class="container px-2">
      <div class="sm:hidden">
        <!-- ----- text ---  -->
        <div class="text-end">
          <h1
            class="text-[40px] uppercase md:text-[54px] leading-[120%] font-newYork"
          >
            Afscheid
          </h1>
          <p
            class="font-helvatika capitalize text-[#2D3B3BE5] pb-8 pt-3 text-[14px] md:text-[20px] leading-[150%]"
          >
            Explore a refined selection of my finest work, blending luxury
            aesthetics with artistic precision. From high-end editorial shoots
            to intimate portraits, this portfolio showcases the elegance and
            depth behind every frame.
          </p>
        </div>
        <div class="flex gap-3">
          <div class="space-y-2 max-w-[300px]">
            <div>
              <img class="w-full h-full" :src="i1" alt="" />
            </div>
            <div>
              <img class="min-h-[240px] w-full" :src="i2" alt="" />
            </div>
          </div>
          <div class="overflow-hidden space-y-2.5 max-w-[300px]">
            <div>
              <img class="w-full object-fit-cover" :src="i7" alt="" />
            </div>
            <div>
              <img class="w-full min-h-[260px]" :src="i4" alt="" />
            </div>
          </div>
        </div>
      </div>
      <!-- desktop view  -->
      <div
        class="hidden w-[100%] sm:grid gap-5 grid-cols-[repeat(3,1fr)] grid-rows-[reapeat(3,1fr)]"
      >
        <div class="col-satrt-1 col-end-2 row-span-2">
          <img
            class="w-[100%] min-h-[400px] max-h-auto object-cover"
            :src="i1"
            alt=""
          />
        </div>
        <div class="text-end row-start-1 row-end-2 col-start-2 col-end-4">
          <h1
            class="text-[40px] uppercase md:text-[54px] leading-[120%] font-newYork"
          >
            Afscheid
          </h1>
          <p
            class="font-helvatika capitalize text-[#2D3B3BE5] pb-8 pt-3 text-[14px] md:text-[20px] leading-[150%]"
          >
            Explore a refined selection of my finest work, blending luxury
            aesthetics with artistic precision. From high-end editorial shoots
            to intimate portraits, this portfolio showcases the elegance and
            depth behind every frame.
          </p>
        </div>
        <div class="col-start-[2] col-end-[3] row-start-[2] row-end-[3]">
          <img class="h-[100%] w-[100%]" :src="i2" alt="" />
        </div>
        <div class="col-start-[3] col-end-[4] row-start-[2] row-end-[3]">
          <img class="w-[100%] h-[100%]" :src="i5" alt="" />
        </div>
        <div class="row-start-[3] row-end-[4]">
          <img class="h-[100%] w-[100%]" :src="i3" alt="" />
        </div>
        <div class="row-start-3 row-end-4">
          <img class="w-[100%]" :src="i4" alt="" />
        </div>
        <div class="row-start-3 row-end-4]">
          <img class="h-[100%] w-[100%]" :src="i6" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>
