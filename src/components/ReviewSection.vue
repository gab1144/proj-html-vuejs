<script>

  import ReviewCard from './ReviewCard.vue';
  import reviews from '../data/reviews';

  export default{
    name: 'ReviewSection',
    components:{
      ReviewCard
    },
    data(){
      return{
        reviews
      }
    }
  }
</script>

<template>
  <section class="review">
    <div class="container">
      <h2>Real world results</h2>
      
      <div class="card-area">
        <ReviewCard
          v-for="(review, index) of reviews"
          :key="index"
          :name="review.name"
          :review="review.review"
          :img="review.img"/>
      </div>
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
    .container {
      padding: 100px 0;
      @include sectionContainer();
      flex-direction: column;
      h2 {
        text-transform: uppercase;
        @include divider("xx-red");
        margin-bottom: 20px;
        span {
          text-transform: uppercase;
        }
      }
      > span {
        display: block
      }
    }
    .card-area {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }
  }
</style>