<script setup>
import { ref, watch, reactive, onMounted } from "vue";
import { usePointer } from "@vueuse/core";

const pointer = reactive(usePointer());
const canvas = ref(null);

watch(pointer, () => {
  if (pointer.pressure === 0) return;
  const ctx = canvas.value.getContext("2d");
  ctx.fillStyle = "#00bd7e";
  ctx.fillRect(pointer.x - 35, pointer.y, 10, 10);
});
onMounted(() => {
  canvas.value.width = 1000;
  canvas.value.height = 850;
});
</script>

<template>
  <canvas ref="canvas"></canvas>
  <p>Pointer Values:</p>
  <p>{{ pointer }}</p>
</template>

<style scoped></style>
