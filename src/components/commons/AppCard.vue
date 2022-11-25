<script>
export default {
  name: "AppCard",
  props: {
    img: String,
    alt: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <a href="#"><img :src="img" :alt="alt" /></a>
    <h5>{{ title }}</h5>
  </div>
</template>

<style lang="scss" scoped>
a {
  display: block;
  height: 11.25rem;
  width: 100%;
  img {
    object-fit: cover;
    object-position: top;
    display: block;
    height: 100%;
    width: 100%;
  }
}
h5 {
  margin: 1.25rem 0 3.125rem;
}
</style>
