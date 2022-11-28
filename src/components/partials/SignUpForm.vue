<script>
  export default{
    name: 'SignUpForm'
  }
</script>

<template>
  <div class="form">
    <h3>Sign up for a free training session</h3>
    
    <div>
      <label for="name">Name</label>
      <input type="text" name="name">
    </div>

    <div>
      <label for="email">Email</label>
      <input type="email" name="email">
    </div>

    <div class="button">
      <a href="#">
        Start Now!
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../styles/partials/vars' as *;
  @use '../../styles/partials/mixin' as *;
  .form {
    width: 50%;
    padding: 40px;
    * {
      margin-bottom: 20px;
    }
    label{
      color: $color-cube-edward;
    }
    input {
      width: 100%;
      background-color: $color-cube-shark;
      border: 0.5px solid $color-cube-white;
      padding: 15px;
      margin-top: 10px;
      color: $color-cube-white;
      &:focus {
        outline:none;
      }
    }
    .button{
      background-color: $color-cube-chestnut-rose;
      text-align: center;
      a {
        color: $color-cube-white;
        text-transform: uppercase;
      }
    }
  }
</style>