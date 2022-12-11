<script setup>
import { useInterval } from "@vueuse/core";

// count will increase every 1000ms
const { counter, pause, resume, isActive } = useInterval(1000, {
  controls: true,
});
</script>

<template>
  <div>
    <p>Seconds: {{ counter }}</p>
    <button @click="isActive ? pause() : resume()">
      {{ isActive ? "Pause" : "Resume" }}
    </button>
    <button @click="counter = 0">Reset</button>
  </div>
</template>

<style scoped></style>
