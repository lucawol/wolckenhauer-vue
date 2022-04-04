<template>
  <div>
    <HomeView></HomeView>
  </div>
</template>

<script>
import HomeView from "./views/HomeView.vue"

export default {
  name: 'App',
  components: {
    HomeView,
  }
}
</script>

<style>
  body{
    margin: 0;
    padding: 0;
    background-color: black;
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: white;
  }
  HTML, body {
  margin: 0px;
  padding: 0px;
  border: 0px;
  }





</style>
