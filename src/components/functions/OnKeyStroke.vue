<script setup>
import { ref } from "vue";
import { onKeyStroke } from "@vueuse/core";

const position = ref({ x: 0, y: 0 });

const controls = {
  ArrowDown: () => (position.value.y += 5),
  ArrowUp: () => (position.value.y -= 5),
  ArrowRight: () => (position.value.x += 5),
  ArrowLeft: () => (position.value.x -= 5),
};

onKeyStroke(Object.keys(controls), (e) => {
  e.preventDefault();
  controls[e.key]();
});
</script>

<template>
  <div>
    <div class="container">
      <div
        class="ball"
        :style="{ transform: `translate(${position.x}px, ${position.y}px)` }"
      />
    </div>
    <div class="hint">
      Use the arrow keys to control the movement of the ball.
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 400px;
  height: 100px;
  margin: auto;
  overflow: hidden;
  border: 1px solid #a1a1a130;
  border-radius: 5px;
}

.ball {
  width: 16px;
  height: 16px;
  background: #a1a1a1;
  border-radius: 50%;
}

.hint {
  text-align: center;
  margin-top: 1rem;
}
</style>
