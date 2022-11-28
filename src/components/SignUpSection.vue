<script>

  import SignUpForm from './partials/SignUpForm.vue';

  export default{
    name: 'SignUpSection',
    components:{
      SignUpForm
    }
  }
</script>

<template>
  <section class="sign-up">
    <div class="container">
      <div class="img-area">
        <img src="../assets/img/home_img-compressor.jpg" alt="">
      </div>

      <SignUpForm/>

    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .sign-up{
    background-color: $median-cut-shark;
  }
  .container{
    @include sectionContainer();
    .img-area{
      width: 50%;
      @include centerFlex('vertical');
      img {
        width: 100%;
      }
    }
  }

/******************************
        RESPONSIVE
******************************/
@media screen and (max-width: 767px){
    .container {
      display: flex;
      flex-direction: column;
      > div {
        width: 100%;
      }
      .img-area {
        width: 100%;
      }
    }
  }
</style>