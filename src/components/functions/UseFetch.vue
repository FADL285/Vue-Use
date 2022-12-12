<script setup>
import { useFetch } from "@vueuse/core";
import { ref } from "vue";

const url = ref("https://dummyjson.com/users/add");

const { data, error, isFinished, isFetching, statusCode } = useFetch(url, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    firstName: "Mohamed",
    lastName: "Fadl",
    age: 22,
    username: "fadl285",
    email: "mohamedfadl@mail.com",
    password: "2852000",
  }),
}).json();
</script>

<template>
  <div>
    <p class="error" v-if="error">Error: {{ error }}</p>
    <p class="loading" v-if="isFetching">Loading...</p>
    <div v-if="isFinished && !error">
      <p>Status code: {{ statusCode }}</p>
      <pre lang="json">{{ data }}</pre>
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
