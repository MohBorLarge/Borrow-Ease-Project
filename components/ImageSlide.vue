<template>
  <!-- Info Slide Content -->
  <div
    class="bg-light-bg mx-auto md:px-64 md:mt-20 md:relative md:z-10 text-black"
  >
    <div class="text-center text-gray-text py-20">
      <!-- Slide Start -->
      <div
        class="border w-4/5 mx-auto py-10 mt-6 bg-white rounded-lg border-border-line"
      >
        <div class="flex justify-between w-24 mx-auto text-secondary">
          <Icon name="material-symbols:star-rate" size="20" />
          <Icon name="material-symbols:star-rate" size="20" />
          <Icon name="material-symbols:star-rate" size="20" />
          <Icon name="material-symbols:star-rate" size="20" />
          <Icon name="material-symbols:star-outline" size="20" />
        </div>
        <div class="mx-auto mt-6">
          "I needed a loan urgently, and Borrow Ease came to my rescue. The
          application process was seamless, and I received the funds in no time.
          The team was professional, and their flexible repayment options made
          it easy for me to manage my finances. Highly recommended!"
        </div>
      </div>
      <div class="w-64 mt-4 flex gap-4 mx-auto">
        <img src="assets/icons/human.svg" alt="" />
        <div>
          <p class="text-bold-gray font-bold mt-1.5">Akanbi Taiwo Mayowa</p>
          <p class="float-left">CEO of Workation</p>
        </div>
      </div>
      <!-- Slide End -->

      <div class="w-24 mt-14 mx-auto">
        <Icon
          name="mdi:arrow-left"
          @click="prev()"
          class="cursor-pointer border-0 w-6 h-6 rounded-full text-white bg-primary mr-4"
        />
        <Icon
          name="mdi:arrow-right"
          @click="next()"
          class="cursor-pointer border-0 w-6 h-6 rounded-full text-white bg-primary"
        />
      </div>
    </div>

    <div class="text-white bottom-20 px-10">
      <!-- Info Slide Text -->
      <div class="mb-16">
        <p class="opacity-80 uppercase mb-2.5">Bolaji</p>
        <p class="font-family-medium">Daniel Regah</p>
      </div>

      <!-- Info Slide Footer -->
      <div class="flex items-center w-full justify-between">
        <!-- <div class="flex">
          <div
            v-for="item in authSlides"
            :key="item"
            class="w-8 h-1 rounded-sm bg-white transition ease-in duration-300 mr-2.5 opacity-100 transition ease-in duration-300"
            
          ></div>
        </div> -->
      </div>
    </div>
  </div>
</template>

<script>
// import { useSliderStore } from "~~/stores";

export default {
  setup() {
    const runSlide = () => {
      setInterval(() => {
        next();
      }, 4000);
    };

    const prev = () => {
      console.log("prev");
    };

    const next = () => {
      console.log("next");
    };

    return {
      prev,
      next,
      runSlide,
    };
  },
};
</script>
