<script>

  import TrainerCard from './TrainerCard.vue';
  import trainers from '../data/trainers'
  export default{
    name: 'TrainersSection',
    components:{
      TrainerCard
    },
    data(){
      return{
        trainers
      }
    }
  }
</script>

<template>
  <section class="trainers">
    <div class="container">
      <div class="card-area">
        <TrainerCard
        v-for="(trainer, index) of trainers"
        :key="index"
        :name="trainer.name"
        :description="trainer.description"
        :role="trainer.role"
        :img="trainer.img"
        />
      </div>
      <div>
        <button class="button">
          View all trainers
        </button>
      </div>
    </div>
    <i class="chevron-border-section"></i>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .trainers {
    background-color: $median-cut-shark;
    position: relative;
    .container {
      @include sectionContainer();
      position: relative;
      @include centerFlex('vertical');
      flex-direction: column;
    }
    .card-area {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }
    .button {
      background: none;
      border: 1px solid $color-cube-white;
      color: $color-cube-white;
      text-transform: uppercase;
      width: fit-content;
    }
    .chevron-border-section::before {
      border-top-color: $median-cut-shark;
    }
  }
</style>