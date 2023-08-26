<template>
  <div id="map" style="height: 100vh; width: 100vw" />
</template>

<script setup lang="ts">
import maplibregl from "maplibre-gl";
onMounted(() => {
  new maplibregl.Map({
    container: "map",
    style: "https://basemaps.cartocdn.com/gl/dark-matter-gl-style/style.json",
    center: [0, 0],
    zoom: 1,
  });
});
// const mapRef = ref(null);

// watchEffect(() => {
//   if (mapRef.value) {
//     new maplibregl.Map({
//       container: mapRef.value!,
//       style: "https://basemaps.cartocdn.com/gl/dark-matter-gl-style/style.json",
//       center: [0, 0],
//       zoom: 1,
//     });
//   } else {
//     // not mounted yet, or the element was unmounted (e.g. by v-if)
//   }
// });
</script>

<style>
* {
  margin: 0;
  padding: 0;
  overflow: hidden;
  background: rgba(0, 0, 0, 0.33);
}
</style>
