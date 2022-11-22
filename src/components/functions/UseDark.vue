<script setup>
import { useDark, useToggle } from "@vueuse/core";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <button @click="toggleDark()">
    <span>Switch to {{ isDark ? "Light" : "Dark" }}</span>
  </button>
</template>
