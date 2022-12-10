<script setup>
import { ref } from "vue";
import { useInfiniteScroll } from "@vueuse/core";

const el = ref(null);
const data = ref([]);
const total = ref(0);

async function fetchData() {
  if (data.value.length !== 0 && data.value.length >= total.value) {
    console.log("no more data");
    return;
  }
  console.log("fetching data", data.value.length);
  const res = await fetch(
    `https://dummyjson.com/products/?limit=10&skip=${data.value.length}`
  );
  const resData = await res.json();
  console.log(resData);
  total.value = resData.total;
  data.value = data.value.concat(resData.products);
}

useInfiniteScroll(el, fetchData, { distance: 50 });

fetchData();
</script>

<template>
  <div class="wrapper" ref="el">
    <div class="card" v-for="item in data" :key="item.id">
      <img :src="item.thumbnail" :alt="item.title" />
      <h3>{{ item.title }}</h3>
      <p class="desc">{{ item.description }}</p>
      <p class="price">
        Price <span class="price--total">${{ item.price }}</span>
      </p>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 1rem;
  padding: 1rem;
  height: 100vh;
  overflow-y: auto;
}

.card {
  background: #222121;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  padding: 1rem;
  display: flex;
  flex-direction: column;
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 5px;
}

.card h3 {
  margin: 1rem 0;
  font-size: 1.75rem;
  color: #fff;
}

.card .desc {
  color: #e0e0e0;
  margin-bottom: 1rem;
}

.card .price {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: auto;
}

.card .price--total {
  color: #00bd6e;
  font-weight: bold;
}
</style>
