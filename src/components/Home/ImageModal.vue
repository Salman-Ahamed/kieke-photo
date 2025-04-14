<script setup lang="ts">
defineProps<{ show: boolean; imageUrl: string }>();
defineEmits<{ close: [] }>();
</script>

<template>
  <div
    v-if="show"
    class="fixed top-0 left-0 bg-black/30 backdrop-blur-[2px] w-screen h-screen bg-opacity-80 z-50 flex items-center justify-center"
  >
    <div class="relative">
      <div class="fixed top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
        <img
          :src="imageUrl"
          class="min-w-[300px] md:min-w-[500px] max-w-[300px] md:max-w-[500px] min-h-[300px] md:min-h-[500px] max-h-[300px] md:max-h-[500px] object-cover rounded"
        />
        <button
          @click="$emit('close')"
          class="absolute size-[30px] cursor-pointer rounded-full top-2 right-2 bg-black/50 text-white text-xl"
        >
          ✕
        </button>
      </div>
    </div>
  </div>
</template>
