<script>

  import facilities from '../data/facilities';

  export default{
    name: 'FacilitiesSection',
    data(){
      return{
        facilities
      }
    },
    methods:{
      getImagePath(imageName){
        return new URL(`../assets/img/${imageName}`, import.meta.url).href
      }
    }
  }
</script>

<template>
  <section class="facilities">
    <div class="container">
      <h2>High performance facilities</h2>
      
      <div class="img-area">
        <img 
        v-for="facilitie of facilities"
        :src="getImagePath(facilitie.img)" :alt="facilitie.name">
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .facilities {
    background-color: $color-cube-shark;
    text-align: center;
    position: relative;
    .container {
      padding: 100px 0;
      @include sectionContainer();
      flex-direction: column;
      h2 {
        text-transform: uppercase;
        @include divider("xx-red");
        margin-bottom: 20px;
      }
      .img-area {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        img {
          width: calc(calc(100% - 50px) / 3);
          margin-bottom: 25px;
          transition: 0.5s ;
          &:hover {
            transform: scale(1.05);
          }
        }
      }
    }
  }
</style>