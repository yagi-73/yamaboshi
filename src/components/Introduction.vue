<template>
<FadeIn>
  <div class="introduction">
    <div class="illust">
      <img alt="ヤマボウシ" src="../assets/yamaboshi-left.jpg">
    </div>
    <div>
      <img alt="logo" src="../assets/logo.jpg">
        <p>
          手打蕎麦 山ぼうしは大和市にある美味しいお蕎麦を楽しむことのできるお店です。<br>
          お蕎麦の前に、ちょっとした肴をあてに美味い酒を飲みながらゆるりとすごす…<br>
          そんな粋な蕎麦屋酒もお楽しみいただけます。
        </p>
    </div>
      <div class="illust">
        <img alt="ヤマボウシ" src="../assets/yamaboshi-right.jpg">
      </div>
</div>
</FadeIn>
</template>
<script>
  import FadeIn from './FadeIn.vue'
  export default {
    name: 'Introduction',
    components: {
      FadeIn
    }
  }
</script>
<style>
  .introduction {
    display: flex;
    height: 400px;
    width: 90%;
    text-align: center;
    margin: 30px auto;
    font-size: 20px;
    letter-spacing: 3px;
    line-height: 2;
  }
  .illust {
    height: 250px;
    width: 400px;
    margin-top: 70px;
  }
  .illust img {
    width: 100%;
  }
  /* .fade-enter-active, .fade-leave-active {
    will-change: opacity;
    transition: opacity 225ms cubic-bezier(0.4, 0, 0.2, 1) 0ms;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0
  } */
</style>