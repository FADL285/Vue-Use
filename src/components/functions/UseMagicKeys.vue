<script setup>
import { useMagicKeys, whenever } from "@vueuse/core";

const { ctrl_shift_f } = useMagicKeys();
whenever(ctrl_shift_f, (pressed) => {
  console.log(pressed);
  alert("You Pressed Ctrl + Shift + F");
});
</script>

<template>
  <p>Press <kbd>Ctrl + Shift + F</kbd> Keys</p>
</template>

<style>
kbd {
  padding: 0.25rem;
  background: rgba(1, 1, 1, 0.4);
  border-radius: 0.25rem;
}
</style>
