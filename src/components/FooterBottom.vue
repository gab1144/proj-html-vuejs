<script>
  export default{
    name: 'FooterBottom',
  }
</script>

<template>
  <div class="footer-bottom">
    <div class="container">
      <div class="text-area">
        <span>&copy; Copyright 2012 - 2020</span>
        <span>Avada Theme by Theme fusion</span>
        <span>All Rights Reserved</span>
        <span>Powered by WordPress</span>
      </div>

      <div class="social-links-area">
        <div class="social-link">
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
        </div>

        <div class="social-link">
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
        </div>

        <div class="social-link">
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .footer-bottom{
    background-color: $median-cut-shark;
    .container {
      padding: 50px 0;
      display: flex;
      justify-content: space-between;
      color: $color-cube-edward;
      .text-area {
        @include centerFlex('vertical');
      }
      .text-area span:not(:last-of-type)::after{
        content: "|";
        padding: 0 10px;
      }
      .social-links-area {
        display: flex;
      }
      .social-link {
        background-color: $color-cube-chestnut-rose;
      }
    }
  }
</style>