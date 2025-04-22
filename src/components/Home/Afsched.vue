<script setup lang="ts">
import { ref } from "vue";
import i1 from "../../assets/Home/Afsched/i1.png";
import i2 from "../../assets/Home/Afsched/i2.png";
import i3 from "../../assets/Home/Afsched/i3.png";
import i4 from "../../assets/Home/Afsched/i4.png";
import i5 from "../../assets/Home/Afsched/i5.png";
import i6 from "../../assets/Home/Afsched/i6.png";
import i7 from "../../assets/Home/Afsched/i7.png";
import ImageModal from "./ImageModal.vue";

const showModal = ref(false);
const imgUrl = ref<string>("");

const closeModal = () => {
  showModal.value = false;
};

const imageUrl = (url: string) => {
  imgUrl.value = url;
  showModal.value = true;
};
</script>

<template>
  <section class="pt-4 md:pt-10 lg:pt-20 pb-5" id="afscheid">
    <div class="container px-2">
      <div class="sm:hidden">
        <!-- ----- text ---  -->
        <div class="text-end">
          <h1
            class="text-[40px] uppercase md:text-[54px] leading-[120%] font-newYork"
          >
            Afsc<span class="text-[#2D3B3BB2]">heid</span>
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
              <img
                @click="imageUrl(i1)"
                class="w-full h-full cursor-pointer"
                :src="i1"
                alt=""
              />
            </div>
            <div>
              <img
                class="min-h-[240px] w-full cursor-pointer"
                @click="imageUrl(i2)"
                :src="i2"
                alt=""
              />
            </div>
          </div>
          <div class="overflow-hidden space-y-2.5 max-w-[300px]">
            <div>
              <img
                class="w-full object-fit-cover cursor-pointer"
                :src="i7"
                @click="imageUrl(i7)"
                alt=""
              />
            </div>
            <div>
              <img
                class="w-full min-h-[260px] cursor-pointer"
                :src="i4"
                @click="imageUrl(i4)"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
      <!-- desktop view  -->
      <div
        class="hidden w-full sm:grid gap-5 grid-cols-[repeat(3,1fr)] grid-rows-[reapeat(3,1fr)]"
      >
        <div class="col-satrt-1 col-end-2 row-span-2">
          <img
            class="w-full min-h-[400px] max-h-auto object-cover cursor-pointer"
            @click="imageUrl(i1)"
            :src="i1"
            alt=""
          />
        </div>
        <div class="text-end row-start-1 row-end-2 col-start-2 col-end-4">
          <h1
            class="text-[40px] uppercase md:text-[54px] leading-[120%] font-newYork"
          >
            Afsc<span class="text-[#2D3B3BB2]">heid</span>
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
          <img
            @click="imageUrl(i2)"
            class="h-full w-full cursor-pointer"
            :src="i2"
            alt=""
          />
        </div>
        <div class="col-start-[3] col-end-[4] row-start-[2] row-end-[3]">
          <img
            @click="imageUrl(i5)"
            class="w-full h-full cursor-pointer"
            :src="i5"
            alt=""
          />
        </div>
        <div class="row-start-[3] row-end-[4]">
          <img
            class="h-full w-full cursor-pointer"
            @click="imageUrl(i3)"
            :src="i3"
            alt=""
          />
        </div>
        <div class="row-start-3 row-end-4">
          <img
            class="w-full cursor-pointer"
            @click="imageUrl(i4)"
            :src="i4"
            alt=""
          />
        </div>
        <div class="row-start-3 row-end-4]">
          <img
            class="h-full w-full cursor-pointer"
            @click="imageUrl(i6)"
            :src="i6"
            alt=""
          />
        </div>
      </div>
      <!-- ------------ modal --------------  -->
      <ImageModal :show="showModal" :image-url="imgUrl" @close="closeModal" />
    </div>
  </section>
</template>
