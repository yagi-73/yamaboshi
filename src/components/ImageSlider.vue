<template>
    <transition-group tag="ul" class="slide-fade">
      <li v-for="slide in slides" :key="slide" :class="['slide'+slide, 'item']"></li>
    </transition-group>
    <div :class="['scroll', {isActive : scrollY < 400}]">
      <!-- <span class="txt">Scroll</span> -->
    </div>
</template>
<script>
export default {
  name: 'ImageSlider',
  data() {
    return {
      slides: [1],
      i: 2,
      scrollY: 0
    }
  },

  mounted() {
    setInterval(async () => {this.startSlide()}, 3000),
    window.addEventListener('scroll', this.handleScroll)
  },

  methods: {
    startSlide: function() {
      this.slides.shift()
      this.slides.splice(0, 1, this.i)
      this.i++;
      if (this.i > 3) {
        this.i = 1;
      }
    },
    handleScroll() {
      this.scrollY = window.scrollY
    }
  }
}
</script>

<style>
  .item {
    width: 100%;
    height: 100%;
    background-size: cover;
    background-position: center;
    position: absolute;
    overflow: hidden;
    border-radius: 0 0 100% 100% / 15%;
  }
  .slide-fade {
    width: 100%;
    height: 850px;
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
  .scroll {
    display: inline-block;
    visibility: hidden;
    margin: 15px 0 40px 0;
    position: relative;
  }
  .scroll::before {
    animation: scroll 3.0s infinite;
    border: solid #000;
    border-width: 0 0 1px 1px;
    content: "";
    display: inline-block;
    margin: auto;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    transform: rotate(-45deg);
    width: 20px;
    height: 20px;
  }
  .isActive {
    visibility: visible;
  }
  @keyframes scroll {
    0% {
      transform: rotate(-45deg) translate(0, 0);
    }
    80% {
      transform: rotate(-45deg) translate(-30px, 30px);
    }
    0%, 80%, 100% {
      opacity: 0;
    }
    40% {
      opacity: 1;
    }
  }
</style>