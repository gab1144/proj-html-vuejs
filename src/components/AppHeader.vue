<script>

  import menu from '../data/header-menu';

  export default{
    name: 'AppHeader',
    data(){
      return{
        menu
      }
    }
  }
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/gym_logo_2x.png" alt="Logo Avada Gym">
      </div>
  
      <nav>
        <ul>
          <li
          v-for="(link, index) in menu"
          :key="index">
            <a :class="{'active': link.current}" :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
  header{
    height: 100px;
    width: 100%;
    .container{
      @include vCenterSpcBtw();
      max-width: none;
      width: 100%;
      padding: 20px;
      .logo img{
        height: 80px;
      }
      ul {
        display: flex;
        list-style: none;
      }
      li {
        padding: 0 20px;
        &:hover{
          color: $color-cube-chestnut-rose;
        }
      }
      a {
        text-decoration: none;
        text-transform: uppercase;
        display: inline-block;
        color: white;
          &:hover,
          &.active{
          color: $color-cube-chestnut-rose;
          }
      }
    }
  }
</style>