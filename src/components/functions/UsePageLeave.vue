<script setup>
import { usePageLeave } from "@vueuse/core";

const isLeft = usePageLeave();
</script>

<template>
  <p>Reactive state to show whether the mouse leaves the page.</p>
  <p class="lg-p">
    is Left: <span class="state">{{ isLeft }}</span>
  </p>
</template>

<style scoped>
.state {
  padding: 0.25rem 0.5rem;
  background: rgb(1 1 1 / 15%);
  border-radius: 0.25rem;
}
</style>
