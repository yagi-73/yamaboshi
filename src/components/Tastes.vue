<template>
  <section class="section-1">
    <div class="transmission"></div>
    <div class="tastes">
      <div class="img-box">
        <FadeIn>
        <img alt="soba" src="../assets/soba.jpg">
        </FadeIn>
      </div>
      <div class="text-box">
        <FadeIn>
        <h1>こだわりの味</h1>
        <p>
          厳選した素材を使用した至極の手打蕎麦・・・。<br>
          当店では国内産高級そば粉を使用し、店主がその日の分を懇切丁寧に<br>
          仕上げた数量限定こだわりの二八蕎麦を提供しております。
        </p>
        <p>
          つゆは厳選された鰹節のみを使用した一番ダシに<br>
          熟成された本かえしをあわせた江戸前の辛汁となっております。<br>
          少量つけてお召し上がりくださいませ。
        </p>
        <p>
          尚、薬味はわさび、大根おろし、ねぎの3種類がついていますが、<br>
          つゆには直接いれず、お蕎麦にのせてお召し上がりいただくことを<br>
          推奨させていただいております。食後に濃厚な蕎麦湯もお楽しみくださいませ。
        </p>
        </FadeIn>
      </div>
    </div>
  </section>
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
<style scoped>
  p {
    margin: 20px 0;
  }
  .section-1 {
    height: 850px;
    width: 100%;
    margin-top: 30px;
    position: relative;
    transform: skewY(5deg) scaleX(-1);
  }
  .section-1::before {
    content: "";
    height: 850px;
    width: 62%;
    position: absolute;
    right: 0;
    left: 0;
    margin: auto;
    background-image: url(../assets/seigaiha.gif);
  }
  .transmission {
    height: 100%;
    width: 62%;
    right: 0;
    left: 0;
    margin: auto;
    position: absolute;
    background: rgba(255,255,255,0.7);
  }
  .tastes img {
    width: 100%;
  }
  .img-box, .text-box {
    width: 50%;
  }
  .tastes {
    display: flex;
    align-items: center;
    height: 100%;
    width: 80%;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    transform: skewY(5deg) scaleX(-1);
  }
  .text-box {
    padding: 120px 40px;
    height: 650px;
    margin-top: 150px;
    text-align: left;
    font-size: 18px;
    font-weight: bold;
  }
  h1:after {
    content: "";
    width: 50px;
    height: 1px;
    background-color: #ddd;
    display: block;
    margin: 15px 0 25px;
}
</style>