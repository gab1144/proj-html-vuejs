<script>

  import contactInfo from '../data/contact-information';
  import news from '../data/news';
  import openingTimes from '../data/opening-times';

  export default{
    name: 'FooterTop',
    data(){
      return{
        contactInfo,
        news,
        openingTimes
      }
    },
    methods:{
      getImagePath(imageName){
        return new URL(`../assets/img/${imageName}`, import.meta.url).href
      }
    }
  }
</script>

<template>
  <div class="footer-top">
    <div class="container">
      <div class="contacts">
        <h4>Come find us</h4>
        <ul>
          <li>{{contactInfo.street}}</li>
          <li>{{contactInfo.city}}</li>
          <li>Phone: {{contactInfo.phone}}</li>
          <li>Email: {{contactInfo.email}}</li>
        </ul>
      </div>

      <div class="recent-posts">
        <h4>Recent posts</h4>
        <details>
          <summary><span class="summary-title">{{news[0].title}}</span></summary>
          <p>{{news[0].content}}</p>
        </details>

        <details>
          <summary><span class="summary-title">{{news[2].title}}</span></summary>
          <p>{{news[2].content}}</p>
        </details>
      </div>

      <div class="opening-times">
        <h4>Opening times</h4>
        <div 
        v-for="(time, index) of openingTimes">
          <span class="day">{{time.days}}</span>
          <span class="time">{{time.times}}</span>
        </div>
      </div>

      <div class="monthly-special">
        <img :src="getImagePath('gym_ad-compressor.jpg')" alt="">
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .footer-top{
    background-color: $color-cube-shark;
    .container {
      padding: 50px 0;
      display: flex;
      color: $color-cube-edward;
      > div {
        width: calc(100% / 4);
        padding: 0 10px;
      }
      h4 {
        text-transform: uppercase;
        font-weight: 100;
        color: $color-cube-dove-grey;
      }
      ul {
        list-style: none;
        margin-top: 20px;
        li {
          margin-top: 10px;
        }
      }
      details p {
        padding-top: 15px;
      }
      details {
        border-bottom: 1px solid $color-cube-dove-grey;
        padding: 15px 0;
      }
      details > summary {
        list-style-type: none;
        display: flex;
      }
      details[open] > summary {
        list-style-type: none;
      }
      details > summary::before {
        content: "\f054";
        font-family: FontAwesome;
        font-size: 12px;
      }
      details[open] > summary::before {
        content: "\f078";
        font-family: FontAwesome;
        font-size: 12px;
        display: inline;
      }
      .summary-title {
        display: inline;
        font-family: 'Josefin Sans', sans-serif;
        width: calc(100% - 20px);
        padding-left: 5px;
        font-size: 18px;
      }
      .day,
      .time {
        display: block;
      }
      .time {
        color: $color-cube-dove-grey;
      }
    }
  }

/******************************
        RESPONSIVE
******************************/
  @media screen and (max-width: 991px){
    .container {
      flex-wrap: wrap;
      > div {
        min-width: calc(100% / 2);
        padding: 0 10px;
      }
    }
  }

  @media screen and (max-width: 767px){
    .container {
      flex-wrap: wrap;
      > div {
        min-width: 100%;
        margin: 20px 0;
      }
    }
  }
</style>