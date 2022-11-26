<script>
  export default{
    name: 'NewsCard',
    props:{
      title: String,
      content: String,
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
  <div class="trainer-card">
    <div class="img-area">
      <img :src="getImagePath(img)" :alt="title">
    </div>

    <div class="text-area">
      <h3>{{title}}</h3>
      <p>{{content}}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;

  .trainer-card{
    width: calc(calc(100% - 100px) /3);
    background-color: $median-cut-shark;
    margin-bottom: 30px;
    .img-area{
      img{
        width: 100%;
      }
    }
    .text-area{
      padding: 30px;
      padding-bottom: 0;
      p {
        margin: 30px 0;
      }
    }
    .link-area{
      margin-top: 30px;
      display: flex;
      flex-wrap: wrap;
      .social-link {
        @include centerFlex();
        min-width: 50px;
        aspect-ratio: 1;
        background-color: $material-design-wooksmoke;
        margin-right: 10px;
        margin-bottom: 30px;
        border-radius: 5px;
      }
    }
  }
  </style>