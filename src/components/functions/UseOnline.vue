<script setup>
import { useOnline } from "@vueuse/core";

const online = useOnline();
</script>

<template>
  <p>Online: {{ online }}</p>
</template>
