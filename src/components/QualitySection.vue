<script>
  export default{
    name: 'QualitySection'
  }
</script>

<template>
  <section class="quality">
    <div class="container">
        <h2><span>World class</span> Fitness</h2>

        <span>At Avada Gym, everything we do from top to bottom is of the highest quality to ensure we're equipped to help you reach your goals of a healthy and fit lifestyle.</span>
    </div>

    <i class="chevron"></i>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .quality {
    background-color: $color-cube-shark;
    text-align: center;
    position: relative;
    .container {
      padding: 100px 0;
      @include centerFlex('both');
      flex-direction: column;
      h2 {
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
    .chevron {
    position:relative;
    bottom: -50px;
    left: calc(50% - 25px);
    display:block;
    height:50px;
    }
    .chevron::before,
    .chevron::after {
      position:absolute;
      display:block;
      content:"";
      border:25px solid transparent; //chevron size
    }
    .chevron::before {
      top:0;
      border-top-color: $color-cube-shark; //chevron Color
    }
  }
</style>