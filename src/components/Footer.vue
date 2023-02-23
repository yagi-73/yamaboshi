<template>
  <footer class="footer">
    <p class="copyright">© 手打蕎麦 山ぼうし. All Rights Reserved.</p>
    <ul class="md-flex">
      <li><a href="#">About</a></li>
      <li><a href="#">サイトマップ</a></li>
      <li><a href="#">プライバシーポリシー</a></li>
    </ul>
  </footer>
</template>
<script>
  export default {
    name: 'Footer',
  }
</script>
<style scoped>
  a {
    color: #999;
    text-decoration: none;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  .footer {
    padding: 2rem;
    font-size: 15px;
    color: #999;
    background: #fff;
    border-top: 1px solid #e5e7eb;
  }

  .footer a:hover {
    color: #000;
  }

  @media (min-width: 768px) {
    .footer {
      display: flex;
      justify-content: space-between;
    }

    .md-flex {
      display: flex;
    }

    .md-flex li + li {
      margin-left: 16px;
    }
  }
</style>