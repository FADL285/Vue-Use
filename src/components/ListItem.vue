<script setup>
defineProps({
  id: Number,
});
</script>

<template>
  <li>{{ id }}</li>
</template>

<style scoped>
li {
  border-bottom: 1px solid;
  padding: 7px;
}
</style>
