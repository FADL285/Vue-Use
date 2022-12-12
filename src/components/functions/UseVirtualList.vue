<script setup>
import { ref } from "vue";
import { useVirtualList } from "@vueuse/core";
import ListItem from "@/components/ListItem.vue";

const longList = ref(Array.from(Array(1000_000).keys()));
const { list, containerProps, wrapperProps } = useVirtualList(longList, {
  itemHeight: 40,
  overscan: 10,
});
</script>

<template>
  <div class="list-container" v-bind="containerProps">
    <ul v-bind="wrapperProps">
      <ListItem v-for="item in list" :id="item.data" :key="item.data" />
    </ul>
  </div>
</template>

<style scoped>
.list-container {
  height: 500px;
  overflow-y: auto;
  border: 1px solid #ccc;
}
</style>
