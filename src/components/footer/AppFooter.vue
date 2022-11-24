<script>
import PreFooter from './PreFooter.vue';
import FooterContacts from './FooterContacts.vue';


export default {
  components: {
    PreFooter,
    FooterContacts,
  }
}
</script>

<template>
    <footer>
        <PreFooter/>
        <FooterContacts/>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-color: var(--darkest-color-light);
}
</style>
