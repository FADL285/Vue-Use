<script setup>
import { refAutoReset } from "@vueuse/core";

const message = refAutoReset("default message", 3000);

const setMessage = () => {
  // here the value will change to 'message has set' but after 3000ms, it will change to 'default message'
  message.value = "message has set";
};
</script>

<template>
  <div>
    {{ message }}
    <button @click="setMessage">Set Message</button>
  </div>
</template>

<style scoped></style>
