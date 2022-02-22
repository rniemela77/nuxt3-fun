<template>
  <div>
    <h1>Other Page</h1>
    <p>{{ width }} {{ height }}</p>
    <img loading="lazy" :src="imgUrl" alt="" :height="height" :width="width" />
  </div>
</template>

<script setup lang="ts">
const imgUrl = ref(null);
const height = ref(0);
const width = ref(0);

onMounted(() => {
  width.value = getRandomInt(300) + 400;
  height.value = getRandomInt(300) + 400;
  imgUrl.value = `https://placebear.com/${width.value}/${height.value}`;
});

function getRandomInt(max: number) {
  return Math.floor(Math.random() * max);
}
// https://placebear.com/
// import Nav from "~/components/Nav.vue";
</script>
