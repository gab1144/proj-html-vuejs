<script>
  export default{
    name: 'TraineCard',
    props:{
      name: String,
      description: String,
      role: String,
      img: String,
      links: Object
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
      <img :src="getImagePath(img)" :alt="name">
    </div>

    <div class="text-area">
      <h3>{{name}}</h3>
      <h3>{{role}}</h3>
      <p>{{description}}</p>
      
      <div class="link-area">
        <div class="social-link">
          <a :href="links.facebook"><i class="fa-brands fa-facebook-f"></i></a>
        </div>

        <div class="social-link">
          <a :href="links.twitter"><i class="fa-brands fa-twitter"></i></a>
        </div>

        <div class="social-link">
          <a :href="links.instagram"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;

  .trainer-card{
    width: calc(calc(100% - 100px) /3);
    background-color: $color-cube-shark;
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
        margin-bottom: 30px;
      }
    }
  }
  </style>