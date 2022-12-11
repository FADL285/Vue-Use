<script setup>
import { ref } from "vue";
import { useDateFormat, useNow } from "@vueuse/core";

const formatter = ref("dddd YYYY-MM-DD hh:mm:ss A");
const formatted = useDateFormat(useNow(), formatter);
</script>

<template>
  <p class="time font-bold text-primary">
    {{ formatted }}
  </p>
  <div class="flex items-center">
    <span class=""> Formatter Editor : </span>
    <input v-model="formatter" type="text" />
  </div>
</template>

<style scoped>
.time {
  font-size: 2rem;
}

.font-bold {
  font-weight: 700;
}

.text-primary {
  color: #2fad75;
}
</style>
