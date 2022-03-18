<template>

<div>
  <div class="navbar">
    <div class="navbar-item">
      Home
    </div>
    <div class="navbar-item">
      About
    </div>
    <div class="navbar-item">
      Contact
    </div>
  </div>
</div>
  
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
  body{
    margin: 0;
  }
  .navbar-container{

  }
  .navbar{
    display: flex;
    position: fixed;
    left: 0;
    border: black solid 1em;
    width: calc(100% - 2em)
  }
  .navbar-item{
    margin-right: 1em;
  }

</style>
