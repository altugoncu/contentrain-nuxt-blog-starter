<template>
  <footer class="bg-black p-4 text-gray-100 flex justify-center items-center">
    <p class="custom-text"> Meshk Music, created by Altuğ Öncü.</p>
  </footer>
</template>

<script setup>
const { data } = await useAsyncData("footer", () =>
  queryContent("contentrain", "footer").findOne()
);
let footerData = data.value.body[0];
</script>

<style></style>
