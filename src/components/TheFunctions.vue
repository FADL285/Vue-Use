<script setup>
import FunctionItem from "./FunctionItem.vue";
import UseTitle from "./functions/UseTitle.vue";
import UseClipboard from "./functions/UseClipboard.vue";
import UseDark from "./functions/UseDark.vue";
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
    <template #heading>
      <a href="https://vueuse.org/core/usedark/#usedark" target="_blank">
        useDark
      </a>
      &
      <a href="https://vueuse.org/shared/usetoggle/#usetoggle" target="_blank">
        useToggle
      </a>
    </template>

    <UseDark />
  </FunctionItem>
</template>
