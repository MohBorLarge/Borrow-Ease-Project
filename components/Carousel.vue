<template>
  <div class="relative overflow-hidden">
    <div class="flex transition-transform ease-in-out duration-300" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
      <slot></slot>
    </div>
    <div class="flex absolute bottom-0 left-0 right-0 justify-center space-x-2 mt-2">
      <button @click="prevSlide" :disabled="currentIndex === 0" class="btn btn-primary">Previous</button>
      <button @click="nextSlide" :disabled="currentIndex === totalSlides - 1" class="btn btn-primary">Next</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const currentIndex = ref(0);

    function nextSlide() {
      currentIndex.value = (currentIndex.value + 1) % totalSlides;
    }

    function prevSlide() {
      currentIndex.value = (currentIndex.value - 1 + totalSlides) % totalSlides;
    }

    return {
      currentIndex,
      nextSlide,
      prevSlide,
    };
  },
  computed: {
    totalSlides() {
      return this.$slots.default().filter((vnode) => vnode.type !== Comment).length;
    },
  },
};
</script>
