<script>

  import menu from '../data/header-menu';

  export default{
    name: 'AppHeader',
    data(){
      return{
        menu,
        hamburgerMenu: false
      }
    },
    methods: {
      closeHamburgerMenu(){
      this.hamburgerMenu = false;
      },
      openHamburgerMenu(){
        this.hamburgerMenu = true;
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
  
      <nav class="standard-menu">
        <ul>
          <li
          v-for="(link, index) in menu"
          :key="index">
            <a :class="{'active': link.current}" :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>


      <div class="hamburger-button" @click="openHamburgerMenu()">
        <i class="fa-solid fa-bars"></i>
      </div>
      
      <div v-if="hamburgerMenu" class="hamburgerMenu-area">

        <button @click="closeHamburgerMenu()" class="close-hamburgerMenu"><i class="fa-solid fa-xmark"></i></button>
        
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
      width: 90%;
      padding: 20px 0;
      .logo img{
        height: 150px;
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
        color: $color-cube-white;
          &:hover,
          &.active{
          color: $color-cube-chestnut-rose;
          }
      }
    }
  }

  .hamburgerMenu-area{
    position: fixed;
    z-index: 999;
    top: 0;
    right: 0;
    background-color: $material-design-wooksmoke;
    width: 30%;
    min-width: 330px;
    height: 100%;
    flex-direction: column;
    animation: open-info 0.2s linear;
    padding-top: 80px;
    ul {
      display: flex;
      flex-direction: column;
      height: 100%;
      li {
        padding: 20px 0;
        padding-left: 20px;
      }
    }
  }

  @keyframes open-info {
    0%{
      right: -30%;
    }
    100% {
      right: 0px;
    }
  }

  .close-hamburgerMenu {
    width: 30px;
    aspect-ratio: 1;
    background: none;
    border: none;
    font-size: 25px;
    cursor: pointer;
    position: absolute;
    top: 30px;
    right: 30px;
    color: $color-cube-chestnut-rose;
  }

  .hamburger-button{
    display: none;
    color: $color-cube-chestnut-rose;
    font-size: 25px;
    cursor: pointer;
  }

/******************************
        RESPONSIVE
******************************/

@media screen and (max-width: 1299px){
  .hamburger-button{
    display: block;
  }
  .standard-menu{
    display: none;
  }
}

@media screen and (max-width: 575px){
  
}
</style>