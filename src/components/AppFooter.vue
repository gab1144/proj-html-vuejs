<script>

  import FooterTop from './FooterTop.vue';

  export default{
    name: 'AppFooter',
    components:{
      FooterTop
    }
  }
</script>

<template>
  <footer>
    <FooterTop/>
  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;
@use '../styles/partials/mixin' as *;

</style>