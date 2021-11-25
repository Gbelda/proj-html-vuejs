<template>
  <div id="app">
    <site-header />
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader.vue";
export default {
  name: "App",
  components: {
    SiteHeader,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;700&display=swap");
@import "./assets/scss/common.scss";
</style>
