<script setup>
import { useColorMode, useCycleList } from "@vueuse/core";

const mode = useColorMode({
  emitAuto: true,
  modes: {
    contrast: "dark contrast",
    cafe: "cafe",
  },
});

const { next } = useCycleList(["dark", "light", "cafe", "contrast", "auto"], {
  initialValue: mode,
});
</script>

<template>
  <button class="mie-2" @click="next()">
    <span class="capitalize">{{ mode }}</span>
  </button>

  <span class="opacity-50">← Click to change the color mode</span>
</template>

<style>
html.cafe {
  filter: sepia(0.9) hue-rotate(315deg) brightness(0.9);
}

html.contrast {
  filter: contrast(2);
}

.capitalize {
  text-transform: capitalize;
}

.opacity-50 {
  opacity: 0.5;
}

.mie-2 {
  margin-inline-end: 0.5rem;
}
</style>
