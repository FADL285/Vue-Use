<script setup>
import { useTitle } from "@vueuse/core";

const title = useTitle();
console.log(title.value); // print current title
title.value = "Hello VueUse"; // change current title
</script>

<template>
  <div>
    <label for="title">Page Title</label>
    <input type="text" name="title" id="title" v-model="title" />
  </div>
</template>
