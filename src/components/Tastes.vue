<template>
  <section class="section-2">
    <div class="tastes">
      <div class="img-box">
        <img alt="soba" src="../assets/soba.jpg">
      </div>
      <div class="text-box">
        <h2>こだわりの味</h2>
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
          つゆには直接いれず、お蕎麦にのせてお召し上がりいただくことを推奨させて<br>
          いただいております。食後に濃厚な蕎麦湯もお楽しみくださいませ。
        </p>
      </div>
    </div>
  </section>
</template>
<script>
  export default {
    name: 'Introduction',
  }
</script>
<style>
  p {
    margin: 20px;
  }
  .section-2 {
    height: 850px;
    background-image: url(../assets/japanese-paper_00372.jpg);
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
    width: 80%;
    margin: 0 auto;
    margin-top: 30px;
    font-size: 20px;
  }
  .text-box {
    padding: 120px 0;
    height: 650px;
    margin-top: 150px;
    background-color: #fff;
  }
</style>