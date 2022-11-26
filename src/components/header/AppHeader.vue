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
  <header>
    <div class="nav-container container">
      <AppLogo />
      <AppNav />
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  position: sticky;
  top: 0;
  left: 0;
  right: 0;
  background-color: var(--lighter-color);
  z-index: 999;
  box-shadow: 0px 2px 10px 0px #000000;

  .nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
