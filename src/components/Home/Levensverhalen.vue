<script setup lang="ts">
import i1 from "../../assets/Home/Levensverhalen/i1.png";
import i2 from "../../assets/Home/Levensverhalen/i2.png";
import i3 from "../../assets/Home/Levensverhalen/i3.png";
import Donwarrow from "../../assets/icons/dwonarrow.svg";
import Uparrow from "../../assets/icons/uparrow.svg";
import { ref } from "vue";

const articles = ref([
  {
    image: i1,
    title: "The Art of Minimalist Photography: Less is More",
    description:
      "Discover how simplicity can enhance storytelling in photography. This blog explores the power of negative space, clean compositions, and subtle elegance in creating timeless images.",
  },
  {
    image: i2,
    title: "Luxury Through the Lens",
    description:
      "A deep dive into the world of high-end photography, where lighting, composition, and detail transform ordinary moments into extraordinary works of art.",
  },
  {
    image: i3,
    title: "Mastering Light: The Secret to Timeless Photography",
    description:
      "Light is the essence of photography. Learn how to manipulate natural and artificial light to create stunning, high-end visuals that exude sophistication.",
  },
]);

const currentIndex = ref(0);

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % articles.value.length;
};

const prevSlide = () => {
  currentIndex.value =
    currentIndex.value === 0
      ? articles.value.length - 1
      : currentIndex.value - 1;
};
</script>

<template>
  <section class="bg-[#F9F5F466] py-10">
    <div class="container px-2 md:flex gap-10">
      <!-- left side  -->
      <div>
        <div>
          <div class="py-5">
            <h1
              class="text-[40px] md:text-[48px] lg:text-[54px] font-newYork uppercase leading-[120%]"
            >
              Levensver <span class="text-[#2D3B3BE5]">halen</span>
            </h1>
            <p
              class="text-[14px] md:text-[16px] lg:text-[20px] text-[#2D3B3BE5] py-4"
            >
              Dive into the world of photography through insightful articles,
              expert tips, and creative inspiration.
            </p>
          </div>
          <div class="md:flex gap-4">
            <!-- Mobile view -->
            <div class="flex-1 md:hidden">
              <img
                class="w-[100%] max-h-[202px]"
                :src="articles[currentIndex].image"
                alt=""
              />
              <div class="pt-3 pb-4">
                <h1
                  class="text-[#2D3B3BE5] text-[18px] font-[500] md:text-[24px] leading-[140%] capitalize pt-3"
                >
                  {{ articles[currentIndex].title }}
                </h1>
                <p
                  class="text-[#2D3B3BE5] text-[14px] md:text-[18px] leading-[150%] capitalize py-2"
                >
                  {{ articles[currentIndex].description }}
                </p>
              </div>
            </div>
            <!-- Desktop view -->
            <div class="hidden md:block flex-1">
              <img class="w-[100%]" :src="articles[0].image" alt="" />
              <div class="pt-3 pb-4">
                <h1
                  class="text-[#2D3B3BE5] text-[18px] font-[500] md:text-[24px] leading-[140%] capitalize pt-3"
                >
                  {{ articles[0].title }}
                </h1>
                <p
                  class="text-[#2D3B3BE5] text-[14px] md:text-[18px] leading-[150%] capitalize py-2"
                >
                  {{ articles[0].description }}
                </p>
              </div>
            </div>
            <div class="hidden flex-1 w-[100%] md:flex flex-col-reverse">
              <img
                class="max-h-[350px] bg-cover object-fit-content"
                :src="articles[1].image"
                alt=""
              />
              <div>
                <p
                  class="text-[#2D3B3BE5] text-[14px] md:text-[18px] leading-[150%] capitalize py-2"
                >
                  {{ articles[1].description }}
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="flex gap-5 mt-3 md:hidden">
          <button @click="prevSlide">
            <img :src="Donwarrow" alt="Previous" />
          </button>
          <button @click="nextSlide"><img :src="Uparrow" alt="Next" /></button>
        </div>
      </div>

      <!-- right side  -->
      <div class="hidden lg:block">
        <div class="hidden md:flex flex-col">
          <img :src="articles[2].image" alt="" />
          <div>
            <h1
              class="text-[#2D3B3BE5] font-[500] text-[18px] md:text-[24px] leading-[140%] capitalize pt-3"
            >
              {{ articles[2].title }}
            </h1>
            <p
              class="text-[#2D3B3BE5] mb-3 text-[14px] md:text-[18px] leading-[150%] capitalize py-2"
            >
              {{ articles[2].description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
