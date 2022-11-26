<script>
  export default{
    name: 'PerformanceNewsSection',
  }
</script>

<template>
  <section class="performance-news">
    <div class="container">

    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .performance-news {
    @include sectionContainer();
    background-color: $color-cube-shark;
  }
</style>