<script setup>
import FunctionItem from "./FunctionItem.vue";
import UseTitle from "./functions/UseTitle.vue";
import UseClipboard from "./functions/UseClipboard.vue";
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
    <template #heading>
      <a
        href="https://vueuse.org/core/useclipboard/#useclipboard"
        target="_blank"
      >
        useClipboard
      </a>
    </template>

    <UseClipboard />
  </FunctionItem>
  <FunctionItem>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
  </FunctionItem>
</template>
