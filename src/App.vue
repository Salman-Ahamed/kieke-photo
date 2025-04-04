<script setup lang="ts">
import Navbar from "./components/navbar/main.vue";
import Home from "./components/Home/Home.vue";
import Footer from "./components/footer/Footer.vue";
</script>

<template>
  <Navbar />
  <main class="bg-[#FFFFFF]">
    <Home />
  </main>
  <Footer />
</template>

<!-- <style>
::-webkit-scrollbar {
  height: 6px;
}

::-webkit-scrollbar-track {
  background: #1e1e1e;
}

::-webkit-scrollbar-thumb {
  background: #424242;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style> -->
