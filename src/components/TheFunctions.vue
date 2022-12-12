<script setup>
import FunctionItem from "./FunctionItem.vue";
import UseTitle from "./functions/UseTitle.vue";
import UseClipboard from "./functions/UseClipboard.vue";
import UseDark from "./functions/UseDark.vue";
import UseColorMode from "./functions/UseColorMode.vue";
import OnKeyStroke from "./functions/OnKeyStroke.vue";
import UseMagicKeys from "./functions/UseMagicKeys.vue";
import UseOnline from "./functions/UseOnline.vue";
import UseGeolocation from "./functions/UseGeolocation.vue";
import UsePageLeave from "./functions/UsePageLeave.vue";
import UsePointer from "./functions/UsePointer.vue";
import UseScroll from "./functions/UseScroll.vue";
import UseInfiniteScroll from "./functions/UseInfiniteScroll.vue";
import UseDisplayMedia from "./functions/UseDisplayMedia.vue";
import UseInterval from "./functions/UseInterval.vue";
import UseIntervalFn from "./functions/UseIntervalFn.vue";
import UseNow from "./functions/UseNow.vue";
import UseRefHistory from "./functions/UseRefHistory.vue";
import UseFetch from "./functions/UseFetch.vue";
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
  <FunctionItem>
    <template #heading>
      <a
        href="https://vueuse.org/core/usecolormode/#usecolormode"
        target="_blank"
      >
        useColorMode
      </a>
    </template>

    <UseColorMode />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a
        href="https://vueuse.org/core/onkeystroke/#onkeystroke"
        target="_blank"
      >
        onKeyStroke
      </a>
    </template>

    <OnKeyStroke />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a
        href="https://vueuse.org/core/useMagicKeys/#useMagicKeys"
        target="_blank"
      >
        useMagicKeys
      </a>
    </template>

    <UseMagicKeys />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/useBattery/#useBattery" target="_blank">
        useBattery
      </a>
    </template>

    <UseOnline />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a
        href="https://vueuse.org/core/usegeolocation/#usegeolocation"
        target="_blank"
      >
        useGeolocation
      </a>
    </template>

    <UseGeolocation />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a
        href="https://vueuse.org/core/usepageleave/#usepageleave"
        target="_blank"
      >
        usePageLeave
      </a>
    </template>

    <UsePageLeave />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usepointer/#usepointer" target="_blank">
        usePointer
      </a>
    </template>

    <UsePointer />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usescroll/" target="_blank">
        UseScroll
      </a>
    </template>

    <UseScroll />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/useinfinitescroll/" target="_blank">
        UseInfiniteScroll
      </a>
    </template>

    <UseInfiniteScroll />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usedisplaymedia/" target="_blank">
        useDisplayMedia
      </a>
    </template>

    <UseDisplayMedia />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/shared/useinterval" target="_blank">
        useInterval
      </a>
    </template>

    <UseInterval />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/shared/useintervalfn" target="_blank">
        useIntervalFn
      </a>
    </template>

    <UseIntervalFn />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usenow/" target="_blank">
        useNow & useDateFormat
      </a>
    </template>

    <UseNow />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/userefhistory/" target="_blank">
        useRefHistory & useDebounceRefHistory
      </a>
    </template>

    <UseRefHistory />
  </FunctionItem>
  <FunctionItem>
    <template #heading>
      <a href="https://vueuse.org/core/usefetch" target="_blank"> useFetch </a>
    </template>

    <UseFetch />
  </FunctionItem>
</template>
