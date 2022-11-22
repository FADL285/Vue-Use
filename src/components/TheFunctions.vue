<script setup>
import FunctionItem from "./FunctionItem.vue";
import UseTitle from "./functions/UseTitle.vue";
</script>

<template>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usetitle/#usetitle" target="_blank">
        UseTitle
      </a>
    </template>

    <UseTitle />
  </FunctionItem>

  <FunctionItem>
    <template #heading>Tooling</template>

    This project is served and bundled with
  </FunctionItem>
  <FunctionItem>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
  </FunctionItem>
</template>
