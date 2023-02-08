<template>
  <ImageSlider />
  <!-- <div class="main-visual">
  </div> -->
  <img alt="logo" src="./assets/logo.jpg">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import ImageSlider from './components/ImageSlider.vue'

export default {
  name: 'App',
  components: {
    ImageSlider
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: #6c6b6b;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.main-visual {
  width: 100%;
  height: 1000px;
  background-image: url(./assets/appearance.jpg);
  background-size: contain;
  background-position: center;
}
</style>
