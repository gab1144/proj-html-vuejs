<script>
  export default{
    name: 'IconCard',
    props:{
      name: String,
      review: String,
      img: String
    },
    methods:{
      getImagePath(imageName){
        return new URL(`../assets/img/${imageName}`, import.meta.url).href
      }
    }
  }
</script>
<template>
  <div class="review-card">
    <div class="img-area">
      <img :src="getImagePath(img)" :alt="name">
    </div>

    <div class="text-area">
      <p>"{{review}}"</p>
      <span class="name-customer"> - {{name}}</span>
    </div>
  </div>
</template>
<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;

  .review-card {
    display: flex;
    width: calc(calc(100% - 50px) / 2);
    margin-bottom: 30px;
    max-height: 195px;
    background-color: $median-cut-shark;
    color: $color-cube-edward;
    .img-area{
      width: calc(100% / 3);
      min-width: 195px;
      padding: 20px;
      img {
        width: 100%;
      }
    }
    .text-area{
      padding: 20px;
      text-align: left;
      overflow: auto;
      p {
        font-style: italic;
        margin-bottom: 7px;
      }
      .name-customer{
        font-size: 18px;
      }
    }
  }

  @media screen and (max-width: 991px){
    .review-card {
    width: 100%;
    }
  }
</style>