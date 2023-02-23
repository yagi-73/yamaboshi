<template>
  <div class="section-3">
    <div class="inner">
      <h2 class="contact">
        お問い合わせ <img alt="電話番号" src="../assets/tel.png"> 046-260-7755
      </h2>
      <div class="information">
        <div class="map-illustration">
          <img alt="地図" src="../assets/map.jpg">
        </div>
        <table>
          <tbody>
            <tr>
              <td width="20%">所在地</td>
              <td width="80%">
                〒242-0017<br>
                神奈川県大和市大和東3-3-2
              </td>
            </tr>
            <tr>
              <td>営業時間</td>
              <td>
                昼営業 11 : 30 ～ 14 : 00 (L.O. 13 : 30)<br>
                夜営業 17 : 30 ～ 21 : 00 (L.O. 20 : 00)
              </td>
            </tr>
            <tr>
              <td>定休日</td>
              <td>月曜日・第３日曜日</td>
            </tr>
            <tr>
              <td>駐車場</td>
              <td>近隣のコインパーキングをご利用ください。</td>
            </tr>
            <tr>
              <td colspan="2">
                丁寧に仕上げたお蕎麦は数に限りがございます。<br>
                お早目のお越しをお待ち申し上げます。<br>
                お蕎麦がなくなりますと営業終了とさせて頂いております。ご了承くださいませ。
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <dev class="google-map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3249.3125889686803!2d139.46088061560823!3d35.471809049035436!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6018566b49e19b37%3A0x315ed25d160163a9!2z5bGx44G844GG44GX!5e0!3m2!1sja!2sjp!4v1676615047714!5m2!1sja!2sjp"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </dev>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'Information',
  }
</script>
<style scoped>
  .inner {
    width: 80%;
    margin: 0 auto;
    padding-top: 50px;
    text-align: center;
  }
  .contact {
    font-size: 40px;
    letter-spacing: 3px;
  }
  .map-illustration{
    width: 50%;
    margin-right: 2%;
  }
  table {
    width: 48%;
    /* margin-right: 30px; */
  }
  .map-illustration img {
    width: 100%;
  }
  .information {
    width: 100%;
    text-align: left;
    margin-bottom: 50px;
    display: flex;
  }
  table td {
    font-size: 16px;
    padding: 10px;
    letter-spacing: 3px;
    vertical-align: top;
  }
  iframe {
    width: 100%;
    aspect-ratio: 2/1;
  }

  @media (max-width:768px){
    .information {
      display: block;
    }
    .map-illustration, table {
      width: 100%;
    }
  }
</style>