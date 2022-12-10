<script setup>
import { useGeolocation } from "@vueuse/core";

const { coords, locatedAt, error } = useGeolocation();
</script>

<template>
  <pre lang="json">{{
    {
      coords: {
        accuracy: coords.accuracy,
        latitude: coords.latitude,
        longitude: coords.longitude,
        altitude: coords.altitude,
        altitudeAccuracy: coords.altitudeAccuracy,
        heading: coords.heading,
        speed: coords.speed,
      },
      locatedAt,
      error: error?.message,
    }
  }}</pre>
</template>

<style scoped></style>
