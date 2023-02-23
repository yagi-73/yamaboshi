<template>
  <ImageSlider />
  <Introduction />
  <Tastes />
  <Hospitality />
  <div class="shapedividers_com"></div>
  <Information />
  <Footer />
</template>

<script>
import ImageSlider from './components/ImageSlider.vue'
import Introduction from './components/Introduction.vue'
import Tastes from './components/Tastes.vue'
import Hospitality from './components/Hospitality.vue'
import Information from './components/Information.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    ImageSlider,
    Introduction,
    Tastes,
    Hospitality,
    Information,
    Footer
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
  text-align: center;
}
section {
  /* background-image: url(./assets/black_00107.jpg); */
  /* background-image: url(./assets/seigaiha.gif); */
  /* background-color: #FEECD2; */
  /* background-color: black; */
}

</style>