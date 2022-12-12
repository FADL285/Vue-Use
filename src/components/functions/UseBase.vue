<script setup>
import { ref } from "vue";
import { useBase64 } from "@vueuse/core";
const image = ref(null);
const { base64 } = useBase64(image);

const onFileChange = (e) => {
  image.value = e.target.files[0];
};
</script>

<template>
  <div>
    <input type="file" accept="image/*" @change="onFileChange" />
    <br />
    <img :src="base64" alt="image preview" v-if="image" width="200" />
  </div>
</template>

<style scoped></style>
