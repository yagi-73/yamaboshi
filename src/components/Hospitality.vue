<template>
  <section class="section-2">
    <div class="course-meal">
    </div>
    <div class="inner">
        <img alt="最高のおもてなし" src="../assets/hospitality.png">
        <div class="description">
          <p class="text-box">
            <FadeIn>
            当店ではコース料理でのご会食もお楽しみ頂けます。<br>
            ご家族やご友人など大切なひと時をお過ごしくださいませ。<br>
            コース料理はお一人様 税別3800円～<br>
            最後にお蕎麦とデザートがついてきます。<br>
            ２～８名様までご予約承っております。<br>
            お気軽にご相談ください。
            </FadeIn>
          </p>
          <div class="img-box">
            <FadeIn>
            <img alt="デザート" src="../assets/dessert.png">
            </FadeIn>
          </div>
        </div>
    </div>
  </section>
  <div class="shapedividers_com"></div>
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
  .section-2 {
    width: 100%;
    height: 1010px;
    position: relative;
    background-color: #FEECD2;
  }
  .course-meal {
    width: 100%;
    height: 650px;
    margin-top: 60px;
    position: absolute;
    background: url(../assets/course-meal.jpg);
    background-size: cover;
    background-attachment: fixed;
  }
  .inner {
    /* width: 1200px; */
    width: 60%;
    left: 0;
    right: 0;
    margin: auto;
    text-align: right;
    position: absolute;
  }
  .description {
    margin-top: 120px;
    display: flex;
  }
  .text-box {
    margin-top: 120px;
    width: 60%;
    text-align: center;
    font-size: 20px;
    line-height: 2;
  }
  .img-box{
    width: 40%;
  }
  .img-box img {
    width: 100%;
  }
  .shapedividers_com {
    overflow: hidden;
    position: relative;
    height: 100px;
  }

  .shapedividers_com::before {
    content: "";
    position: absolute;
    z-index: 3;
    pointer-events: none;
    background-repeat: no-repeat;
    bottom: -0.1vw;
    left: -0.1vw;
    right: -0.1vw;
    top: -0.1vw;
    transform: scaleX(4);
    transform-origin: 100% 0;
    animation: 10s infinite alternate shape-anim-8266 linear;
    background-size: 100% 100px;
    background-position: 50% 0%;
    background-image: url('data:image/svg+xml;charset=utf8, <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 35.28 2.17" preserveAspectRatio="none"><path d="M0 .5c3.07.55 9.27-.42 16.14 0 6.88.4 13.75.57 19.14-.11V0H0z" fill="%23feecd2"/><path d="M0 1c3.17.8 7.29-.38 10.04-.55 2.75-.17 9.25 1.47 12.67 1.3 3.43-.17 4.65-.84 7.05-.87 2.4-.02 5.52.88 5.52.88V0H0z" opacity=".5" fill="%23feecd2"/><path d="M0 1.85c2.56-.83 7.68-.3 11.79-.42 4.1-.12 6.86-.61 9.58-.28 2.73.33 5.61 1.17 8.61 1 3-.19 4.73-.82 5.3-.84V.1H0z" opacity=".5" fill="%23feecd2"/></svg>');
  }
  @keyframes shape-anim-8266 {
    100% {
      transform: scaleX(4) translateX(calc(100% - (100% / 4)));
    }
  }
  @media (min-width:2100px){
    .shapedividers_com::before{
      background-size: 100% calc(2vw + 90px);
    }
  }
</style>