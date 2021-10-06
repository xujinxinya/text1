<template>
  <div id="app">
    <index />
  </div>
</template>

<script>
import index from "../src/views/index.vue";

export default {
  name: "App",
  components: {
    index,
  },
};
</script>

<style>
@import "./assets/css/base.css";
</style>
