<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";
import Logo from "../../assets/Home/logo.png";
import { navItems } from "../../data/data.ts";

const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId);
  if (element) {
    const elementPosition = element.getBoundingClientRect().top;
    const offsetPosition = elementPosition + window.pageYOffset - 70;
    window.scrollTo({ top: offsetPosition, behavior: "smooth" });
  }
};

const active = ref(0);
const handleActive = (v: number) => (active.value = v);

// Add scroll spy functionality
const updateActiveSection = () => {
  const sections = navItems.map((item) => document.getElementById(item.id));
  const scrollPosition = window.scrollY + 100; // Add offset for header

  sections.forEach((section, index) => {
    if (section) {
      const sectionTop = section.offsetTop;
      const sectionBottom = sectionTop + section.offsetHeight;

      if (scrollPosition >= sectionTop && scrollPosition < sectionBottom) {
        active.value = index;
      }
    }
  });
};

// Add scroll event listener
onMounted(() => {
  window.addEventListener("scroll", updateActiveSection);
  updateActiveSection(); // Initial check
});

// Clean up event listener
onUnmounted(() => {
  window.removeEventListener("scroll", updateActiveSection);
});
</script>

<template>
  <header
    class="p-4 font-Primary border-b border-gray-200 fixed top-0 left-0 right-0 z-50 bg-white/50 backdrop-blur-xl"
  >
    <nav class="container flex justify-between items-center gap-3">
      <div>
        <img :src="Logo" alt="Logo" />
      </div>
      <div class="inline-flex items-center space-x-0.5 md:space-x-2">
        <a
          class="font-[16px] text-nowrap list-unstyled leading-[20.04px] text-[14px] lg:text-[16px] not-first:hidden md:not-first:block font-helvatika cursor-pointer text-black hover:bg-[#F9F5F4] rounded-full px-4 py-2 hover:transition-all hover:duration-300"
          v-for="(item, index) in navItems"
          @click.prevent="scrollToSection(item.id)"
          :key="index"
          @click="handleActive(index)"
          :href="item.id"
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
