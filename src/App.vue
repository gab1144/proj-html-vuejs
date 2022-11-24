<script>

  import AppHeader from './components/AppHeader.vue';
  import Jumbotron from './components/Jumbotron.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    name: 'App',
    components:{
      AppHeader,
      Jumbotron,
      AppMain,
      AppFooter
    }
  }
</script>

<template>
  <div class="banner-background">
    <AppHeader/>
    
    <Jumbotron/>
  </div>
  
  <AppMain/>

  <AppFooter/>

</template>

<style lang="scss">
  @use './styles/general';

  .banner-background{
    background-image: url('./assets/img/home-banner.jpg');
    background-position: top;
  }
</style>
