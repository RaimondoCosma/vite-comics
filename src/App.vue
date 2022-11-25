<script>
import AppHeader from "./components/header/AppHeader.vue";
import AppHero from "./components/hero/AppHero.vue";
import AppMain from "./components/main/AppMain.vue";
import AppFooter from "./components/footer/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppHero,
    AppMain,
    AppFooter,
  },
};
</script>

<template>
  <AppHeader />
  <AppHero />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@import "./style/global.scss";
</style>
