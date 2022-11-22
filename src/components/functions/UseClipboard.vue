<script setup>
import { ref } from "vue";
import { useClipboard, usePermission } from "@vueuse/core";

const input = ref("");
const { text, isSupported, copy, copied } = useClipboard();
const permissionRead = usePermission("clipboard-read");
const permissionWrite = usePermission("clipboard-write");
</script>

<template>
  <div v-if="isSupported">
    <div>
      Clipboard Permission: read <b>{{ permissionRead }}</b> | write
      <b>{{ permissionWrite }}</b>
    </div>
    <p>
      Current copied: <code>{{ text || "none" }}</code>
    </p>
    <input v-model="input" type="text" />
    <button @click="copy(input)">
      <!-- by default, `copied` will be reset in 1.5s -->
      <span v-if="!copied">Copy</span>
      <span v-else>Copied!</span>
    </button>
  </div>
  <p v-else>Your browser does not support Clipboard API</p>
</template>
