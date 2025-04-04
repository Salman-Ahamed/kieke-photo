<script setup lang="ts">
import Logo from "../../assets/Home/logo.png";
import { navItems } from "../../data/data.ts";
import { ref } from "vue";

const active = ref(0);

const handleActive = (v: number) => {
  active.value = v;
};
</script>

<template>
  <header class="p-4 font-Primary border-b border-gray-200">
    <nav class="container flex justify-between items-center gap-3">
      <div>
        <img :src="Logo" alt="Logo" />
      </div>
      <div class="inline-flex items-center space-x-0.5 md:space-x-2">
        <a
          class="font-[16px] text-nowrap list-unstyled leading-[20.04px] text-[14px] lg:text-[16px] not-first:hidden md:not-first:block font-helvatika cursor-pointer text-black hover:bg-[#F9F5F4] rounded-full px-4 py-2 hover:transition-all hover:duration-300"
          v-for="(item, index) in navItems"
          :key="index"
          @click="handleActive(index)"
          :class="
            active === index
              ? 'bg-[#F9F5F4] outline outline-black/50 rounded-full px-4 py-2 transition-all duration-300'
              : ''
          "
        >
          {{ item.name }}
        </a>
      </div>
    </nav>
  </header>
</template>
