<script>
  export default{
    name: 'QuoteSection'
  }
</script>

<template>
  <section class="quote">
    <div class="container">
      <p>"I fear not the man who practiced 10,000 kicks once, but i fear the man who has practiced one kick 10,000 times"</p>

      <span class="quote-of-day">Bruce Lee</span>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .quote {
    background-image: url("../assets/img/home-testimonial-bg.jpg");
    background-position: center;
    .container {
      padding: 100px 0;
      @include centerFlex("horizontal");
      flex-direction: column;
      text-align: center;
      p {
        width: 50%;
        margin: 0 auto;
        text-transform: uppercase;
        @include divider("white");
        margin-bottom: 20px;
        font-size: 20px;
      }
      .quote-of-day {
        text-transform: uppercase;
        font-size: 15px;
        font-weight: 900;
        &::after{
          content: " \2022  Quote of the day";
        }
      }
    }
  }
</style>