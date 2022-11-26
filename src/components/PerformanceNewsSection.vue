<script>

  import NewsCard from './NewsCard.vue';
  import news from '../data/news'

  export default{
    name: 'PerformanceNewsSection',
    components:{
      NewsCard
    },
    data(){
      return{
        news
      }
    }
  }
</script>

<template>
  <section class="performance-news">
    <div class="container">
      <h2>Performance News</h2>

      <div class="card-area">
        <NewsCard
        v-for="(article, index) of news"
        :key="index"
        :title="article.title"
        :content="article.content"
        :img="article.img"
        />
      </div>

      <button class="button">
        Read all articles
      </button>

    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  .performance-news {
    background-color: $color-cube-shark;
    .container {
      @include sectionContainer();
      @include centerFlex('vertical');
      flex-direction: column;
    }
    h2 {
      text-transform: uppercase;
      @include divider("xx-red");
      margin-bottom: 30px;
    }
    .card-area {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      height: 1300px;
      width: 100%;
    }
    .button {
      background: none;
      border: 1px solid $color-cube-white;
      color: $color-cube-white;
      text-transform: uppercase;
      width: fit-content;
    }
  }
</style>