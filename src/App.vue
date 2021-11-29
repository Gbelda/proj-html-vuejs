<template>
  <div id="app">
    <site-header />
    <!-- ./SITE HEADER -->

    <site-main />
    <!-- ./SITE MAIN -->

    <site-footer />
    <!-- ./SITE FOOTER -->
  </div>
</template>

<script>
import SiteFooter from "./components/SiteFooter.vue";
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
export default {
  name: "App",
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;700&display=swap");
@import "./assets/scss/common.scss";
</style>
