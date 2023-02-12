<template>
    <transition-group tag="ul" class="slide-fade">
      <li v-for="slide in slides" :key="slide" :class="['slide'+slide, 'item']"></li>
    </transition-group>
</template>
<script>
export default {
  name: 'ImageSlider',
  data() {
    return {
      slides: [1],
      i: 2
    }
  },

  mounted: function() {
    setInterval(async () => {this.startSlide()}, 3000)
  },

  methods: {
    startSlide: function() {
      this.slides.shift()
      this.slides.splice(0, 1, this.i)
      this.i++;
      if (this.i > 3) {
        this.i = 1;
      }
    }
  }
}
</script>

<style>
  .item {
    width: 100%;
    height: 900px;
    background-size: contain;
    background-position: center;
    position: absolute;
  }
  .slide-fade {
    width: 100%;
    height: 900px;
    position: relative;
  }
  .slide1 {
    background-image: url(../assets/appearance.jpg);
  }
  .slide2 {
    background-image: url(../assets/sample1.jpg);
  }
  .slide3 {
    background-image: url(../assets/sample2.jpg);
  }

  .v-enter-active, .v-leave-active {
    transition: opacity 2.0s ease;
  }

  .v-enter-from, .v-leave-to {
    opacity: 0;
  }
</style>