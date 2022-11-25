<script>
import AppLogo from "./AppLogo.vue";
import AppNav from "./AppNav.vue";

export default {
  components: {
    AppLogo,
    AppNav,
  },
};
</script>

<template>
  <header class="container">
    <AppLogo />
    <AppNav />
  </header>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
