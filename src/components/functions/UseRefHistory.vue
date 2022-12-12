<script setup>
import { ref } from "vue";
// import { useRefHistory } from "@vueuse/core";
import { useDebouncedRefHistory } from "@vueuse/core";

const input = ref("");
const { history, undo, redo, canUndo, canRedo } = useDebouncedRefHistory(
  input,
  {
    debounce: 800,
    capacity: 10,
  }
);
</script>

<template>
  <div>
    <div>
      <input v-model="input" type="text" />
      <button @click="undo" :disabled="!canUndo">Undo</button>
      <button @click="redo" :disabled="!canRedo">Redo</button>
    </div>
    <pre>
      {{ history }}
    </pre>
  </div>
</template>

<style scoped></style>
