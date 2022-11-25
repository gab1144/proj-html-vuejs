<script>
  export default{
    name: 'IconCard',
    props:{
      service: String,
      descritption: String,
      icon: String
    }
  }
</script>
<template>
  <div class="icon-card">
    <div class="icon">
      <i :class="icon"></i>
    </div>

    <h3>{{service}}</h3>
    
    <span class="description">{{descritption}}</span>

  </div>
</template>
<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;

  .icon-card {
    @include centerFlex();
    flex-direction: column;
    width: calc(100% / 4);
    .icon{
      width: 90px;
      aspect-ratio: 1;
      @include centerFlex();
      border: 1px solid $color-cube-chestnut-rose;
      border-radius: 50%;
      padding: 10px;
      font-size: 40px;
      color: $color-cube-chestnut-rose;
    }
    h3 {
      margin: 10px 0;
      @include divider($type: "x-red");
    }
    .description{
      color: $color-cube-edward;
      font-weight: 100;
    }
  }
</style>