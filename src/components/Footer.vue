<template>
    <footer class="site-footer">
      <div class="container footer-inner">
        <div class="footer-column">
          <h5>探索 KKBOX</h5>
          <ul>
            <li><a href="#">特色功能</a></li>
            <li><a href="#">免費聽</a></li>
            <li><a href="#">支援平台</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h5>娛樂情報</h5>
          <ul>
            <li><a href="#">音樂趨勢</a></li>
            <li><a href="#">音樂排行榜</a></li>
          </ul>
        </div>
        <div class="footer-column social">
          <h5>追蹤我們</h5>
          <div class="icons">Facebook • YouTube • Instagram</div>
        </div>
      </div>
    </footer>
</template>

<script setup></script>

<style scoped>
  .site-footer {
    background: var(--footer);
    color: #fff;
    padding: 28px 18px;
    margin-top: 28px;
  }
  .footer-inner {
    display: flex;
    gap: 32px;
  }
  .footer-column h5 {
    margin: 0 0 8px;
  }
  .footer-column ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .footer-column a {
    color: #bfbfbf;
    text-decoration: none;
    font-size: 14px;
  }
</style>