<script setup>
import { watch } from "vue";
import { usePageLeave, whenever } from "@vueuse/core";

const isLeft = usePageLeave();

// ! Watch will fire when the value changes....
watch(isLeft, (value) => {
  console.log("isLeft", value);
});

// ! If i want to fire the watch when the value changes to true, i can use the following: "whenever" from vueuse
/*
whenever(isLeft, () => {
  alert("Are you sure you want to leave?");
});
*/

// ! Improve user experience by ask for confirmation before leaving the page for one time
const unwatch = whenever(isLeft, () => {
  alert("Are you sure you want to leave?");
  unwatch();
});
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
