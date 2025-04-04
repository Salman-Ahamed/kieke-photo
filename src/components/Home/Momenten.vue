<script setup lang="ts">
import img1 from "../../assets/Home/moment/img1.png";
import img2 from "../../assets/Home/moment/img2.png";
import img3 from "../../assets/Home/moment/img3.png";
import Love from "../../assets/icons/love.svg";
import Comment from "../../assets/icons/comment.svg";
import Plain from "../../assets/icons/plane.svg";
import Share from "../../assets/icons/share.svg";
// images for slider
import i1 from "../../assets/Home/moment/i1.png";
import i2 from "../../assets/Home/moment/i2.png";
import i3 from "../../assets/Home/moment/i3.png";
import i4 from "../../assets/Home/moment/i4.png";
import i5 from "../../assets/Home/moment/i5.png";

// ----------------
import { ref, onMounted, onUnmounted, computed } from "vue";

const cardItems = ref([
  {
    image: i1,
    views: "100",
    text: "Light shapes the mood. Shadows create depth. Together, they transform an image into a story....",
  },
  {
    image: i2,
    views: "200",
    text: "Light shapes the mood. Shadows create depth. Together, they transform an image into a story. Here’s a glimpse into the art of lighting perfection. #PhotographyMagic #LightAndShadow #LuxuryVisuals",
  },
  {
    image: i3,
    views: "500",
    text: "Light shapes the mood. Shadows create depth. Together, they transform an image into a story....",
  },
]);
const cardItems2 = ref([
  {
    image: i4,
    views: "100",
    text: "Every image is more than just a photo—it’s a masterpiece. From composition to color harmony, luxury photography is about crafting visual poetry. #LuxuryPhotography #FineArt #VisualElegance",
  },
  {
    image: i5,
    views: "200",
    text: "A portrait isn’t just about capturing a face—it’s about revealing a soul. Every detail, every expression, every emotion carefully framed for timeless impact. #LuxuryPortraits #EleganceInEveryShot #ArtisticVision",
  },
]);

// Duplicate cards to create infinite effect
const duplicatedItems = computed(() => [
  ...cardItems.value,
  ...cardItems.value,
  ...cardItems.value,
]);
const duplicatedItems2 = computed(() => [
  ...cardItems2.value,
  ...cardItems2.value,
]);

const isSmallDevice = ref(window.innerWidth < 768);

const updateDeviceSize = () => {
  isSmallDevice.value = window.innerWidth < 768;
};

onMounted(() => {
  window.addEventListener("resize", updateDeviceSize);
});

onUnmounted(() => {
  window.removeEventListener("resize", updateDeviceSize);
});
</script>

<template>
  <section class="py-10 md:mt-5">
    <div
      class="container h-full px-2 gap-5 md:gap-0 place-items-center md:flex overflow-hidden md:max-h-[850px]"
    >
      <!-- left side  -->
      <div class="flex-[1]">
        <div class="py-2">
          <h1
            class="text-[40px] md:text-[46px] lg:text-[54px] leading-[120%] font-newYork"
          >
            Bijzondere <span class="text-[#2D3B3BB2]">Momenten</span>
          </h1>
          <p
            class="text-[14px] max-w-[500px] lg:text-[20px] text-[#2D3B3BE5] mt-2"
          >
            A curated collection of breathtaking visuals that capture moments,
            emotions, and stories.
          </p>
        </div>
        <div class="flex w-[100%] gap-5 sm:gap-7 md:gap-5 mt-5">
          <div class="flex flex-col gap-5 md:gap-6">
            <img class="w-[100%]" :src="img1" alt="" />
            <img class="w-[100%]" :src="img2" alt="" />
          </div>
          <div>
            <img
              class="w-[100%] max-h-[700px] xl:min-w-[340px]"
              :src="img3"
              alt=""
            />
          </div>
        </div>
      </div>
      <!-- right side  -->
      <div
        class="flex-1 bg-[#F9F5F4] md:px-4 flex flex-col place-items-center mt-10 md:mt-0 md:flex-row md:max-h-[800px]"
      >
        <!-- card 1  -->
        <div
          ref="slider"
          class="flex md:flex-col transition-transform duration-500 ease-in-out"
          :class="{
            'animate-horizontal': isSmallDevice,
            'animate-vertical': !isSmallDevice,
          }"
        >
          <div
            v-for="(item, index) in duplicatedItems"
            :key="index"
            class="card max-w-[300px] min-w-[200px] lg:max-w-[390px]"
          >
            <!-- images -->
            <div>
              <img
                class="w-full min-h-[250px] max-h-[250px]"
                :src="item.image"
                alt=""
              />
            </div>
            <!-- icons -->
            <div class="flex justify-between py-2 items-center">
              <div class="flex items-center gap-3">
                <img :src="Love" height="20" width="20" alt="" />
                <img :src="Comment" height="20" width="20" alt="" />
                <img :src="Plain" height="20" width="20" alt="" />
              </div>
              <div>
                <img :src="Share" height="20" width="20" alt="" />
              </div>
            </div>
            <!-- views -->
            <div>
              <p class="text-[10px]">{{ item.views }} views</p>
              <p class="mt-3 text-[9.32px] md:text-[11.67px] leading-[140%]">
                {{ item.text }}
              </p>
            </div>
          </div>
        </div>
        <!-- card 2  -->
        <div
          ref="slider"
          class="flex md:flex-col transition-transform duration-500 ease-in-out"
          :class="{
            'animate-horizontal2': isSmallDevice,
            'animate-vertical2': !isSmallDevice,
          }"
        >
          <div
            v-for="(item, index) in duplicatedItems2"
            :key="index"
            class="card py-2 px-2 max-w-[300px] min-w-[200px] lg:max-w-[390px]"
          >
            <!-- images  -->
            <div>
              <img class="w-full max-h-[250px]" :src="item.image" alt="" />
            </div>
            <!-- icons  -->
            <div class="flex justify-between py-2 items-center">
              <div class="flex items-center gap-3">
                <img :src="Love" height="20" width="20" alt="" />
                <img :src="Comment" height="20" width="20" alt="" />
                <img :src="Plain" height="20" width="20" alt="" />
              </div>
              <div>
                <img :src="Share" height="20" width="20" alt="" />
              </div>
            </div>
            <!-- views  -->
            <div>
              <p class="text-[10px]">{{ item.views }} views</p>
              <p class="mt-3 text-[9.32px] md:text-[11.67px] leading-[140%]">
                {{ item.text }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
