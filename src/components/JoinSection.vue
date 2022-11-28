<script>
  export default{
    name: 'JoinSection'
  }
</script>

<template>
  <section class="join">
    <div class="container">
      <div class="text-area">
        <h2>Achieve Your Fitness Goals</h2>
        <span>Flexible membership packages to suit all levels of athlete and achive your fitness goals</span>
      </div>
      <div class="button-area">
        <div class="button"><a href="#">Join us</a></div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .join {
    background-image: url("../assets/img/home-parallax.jpg");
    background-position: top;
    .container {
      @include sectionContainer();
      display: flex;

      .text-area {
        width: 70%;
      }
      .button-area {
        width: 30%;
        @include centerFlex('horizontal');
        .button {
          width: fit-content;
          height: fit-content;
          background: none;
          border: 1px solid $color-cube-white;
          text-transform: uppercase;
        }
        a {
          color: $color-cube-white;
        }
      }

    }
  }
</style>