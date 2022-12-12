<script setup>
import { useCycleList } from "@vueuse/core";

const { state, next, prev } = useCycleList([
  "https://tinyurl.com/2p8dav94",
  "https://tinyurl.com/2p9yrrhs",
  "https://tinyurl.com/ycxurpah",
]);
</script>

<template>
  <div class="carousel">
    <transition>
      <img :src="state" alt="" :key="state" />
    </transition>
  </div>
  <button @click="prev()">Previous</button>
  <button @click="next()">Next</button>
</template>

<style>
.carousel {
  position: relative;
  height: 200px;
}
img {
  width: 100%;
  position: absolute;
  height: 225px;
  object-fit: cover;
}
.v-enter-active,
.v-leave-active {
  transition: all 0.2s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
