<script>

  import services from '../data/services';
  import IconCard from './IconCard.vue';

  export default{
    name: 'ReviewSection',
    components:{
      IconCard
    },
    data(){
      return{
        services
      }
    }
  }
</script>

<template>
  <section class="review">
    <div class="container">
      <IconCard 
      v-for="(service, index) of services"
      :key="index"
      :service="service.service"
      :descritption="service.description"
      :icon="service.icon"/>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .review {
    background-color: $color-cube-shark;
    text-align: center;
    position: relative;
    background-image: url("../assets/img/gym_bkgd_bw-compressor.jpg");
    background-size: cover;
    background-position: center;
    .container {
      @include sectionContainer();
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>