<script>
export default {
  name: 'Jumbotron'
}
</script>

<template>
  <div class="jumbotron">
    <h1>No pain no gain</h1>
    
    <span>Motivation is what gets you started. Habit is what keeps you going.</span>

    <div class="button"><a href="#">Join us today</a></div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;

  .jumbotron {
    @include centerFlex('both');
    flex-direction: column;
    background-size: cover;
    height: 800px;
    h1 {
      text-transform: uppercase;
      font-size: 75px;
      font-weight: 900;
    }
    span {
      font-weight: 100;
      margin-top: 10px;
      margin-bottom: 30px;
    }
    .button {
      border: 1px solid $color-cube-white;
      text-transform: uppercase;
      font-weight: 500;
      font-size: 15px;
      padding: 10px 25px;
      a {
        color: $color-cube-white;
        text-decoration: none;
        width: 100%;
        height: 100%;
      }
    }
  }
</style>