<template>
  <ImageSlider />
  <Introduction />
  <Tastes />
</template>

<script>
import ImageSlider from './components/ImageSlider.vue'
import Introduction from './components/Introduction.vue'
import Tastes from './components/Tastes.vue'

export default {
  name: 'App',
  components: {
    ImageSlider,
    Introduction,
    Tastes
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
  font-family: "游明朝", YuMincho, "ヒラギノ明朝 ProN W3", "Hiragino Mincho ProN","HG明朝E","MS P明朝","MS 明朝",serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
