<template>
    <transition-group tag="ul" class="slide-fade">
      <li v-for="slide in slides" :key="slide.id" :class="['slide'+slide.id, 'item', {'active' : slide.isActive}]"></li>
      <!-- <li v-if="slides[0].isActive"></li> -->
    </transition-group>
</template>
<script>
export default {
  name: 'ImageSlider',
  data() {
    return {
      slides: [
        { id: 1, isActive: true},
        { id: 2, isActive: false},
        { id: 3, isActive: false}
      ],
      replace: [],
      i: 1
    };
  },

  mounted: function() {
    setInterval(async () => {this.startSlide()}, 3000);
  },

  methods: {
    startSlide: function() {
      this.replace = { id: this.i, isActive: false}
      this.slides.splice(0, this.i, this.replace);

      this.i++;
      if (this.i > 3) {
        this.i = 1;
      }

      this.replace = { id: this.i, isActive: true}
      this.slides.splice(0, this.i, this.replace);
    }
  }
}
</script>

<style>
  .item {
    width: 100%;
    height: 1000px;
    background-size: contain;
    background-position: center;
    position: absolute;
    display: none;
  }
  .slide-fade {
    width: 100%;
    height: 1000px;
    position: relative;
  }
  .active {
    display: block;
  }
  .slide1 {
    background-image: url(../assets/appearance.jpg);
  }
  .slide2 {
    background-image: url(../assets/logo.jpg);
  }
  .slide3 {
    background-image: url(../assets/soba.jpg);
  }

  .v-enter-active, .v-leave-active {
    transition: opacity 2.0s ease;
  }

  .v-enter-from, .v-leave-to {
    opacity: 0;
  }
</style>