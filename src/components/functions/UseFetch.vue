<script setup>
import { useFetch } from "@vueuse/core";
import { ref } from "vue";

const url = ref("https://dummyjson.com/products?limit=5");

const { data, error, isFinished, isFetching, statusCode } = useFetch(url, {
  afterFetch({ data, response }) {
    console.log(data, response);

    return { data, response };
  },
}).json();
</script>

<template>
  <div>
    <p class="error" v-if="error">Error: {{ error }}</p>
    <p class="loading" v-if="isFetching">Loading...</p>
    <div v-if="isFinished && !error">
      <p>Status code: {{ statusCode }}</p>
      <pre>{{ data }}</pre>
    </div>
  </div>
</template>

<style scoped>
.error {
  color: red;
}

.loading {
  color: rgb(44, 162, 44);
}
</style>
