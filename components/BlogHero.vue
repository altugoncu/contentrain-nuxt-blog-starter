<template>
  <div v-if="heroData" class="relative py-4 text-center">
    <div class="absolute inset-0 bg-cover bg-center filter blur-lg hero-bg">
    </div>
    <div class="relative z-10">
      <h3 class="text-yellow-600 text-base font-bold mb-2">
        {{ heroData.subtitle }}
      </h3>
      <p class="text-gray-700 text-base max-w-xl mx-auto text-white">
        {{ heroData.description }}
      </p>
    </div>
  </div>
  <Youtube />
</template>

<script setup>
import Youtube from '~~/components/Youtube.vue'
import altugImage from '../public/altug-ar-3-2.png'
const { data } = await useAsyncData("hero", () =>
  queryContent("contentrain", "hero").findOne()
);
let heroData = data.value.body[0];
</script>

<style></style>