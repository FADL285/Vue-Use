<script setup>
import { ref, watchEffect } from "vue";
import { useDisplayMedia } from "@vueuse/core";

const video = ref(null);
const { stream, enabled } = useDisplayMedia();

watchEffect(() => {
  if (video.value) video.value.srcObject = stream.value;
});
</script>

<template>
  <div class="video-wrapper">
    <div>
      <button @click="enabled = !enabled">
        {{ enabled ? "Stop" : "Start" }} sharing my screen
      </button>
    </div>

    <div>
      <video ref="video" muted autoplay class="video" />
    </div>
  </div>
</template>

<style scoped>
.video-wrapper {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-align: center;
}
.video {
  height: 100%;
  width: 100%;
}
</style>
