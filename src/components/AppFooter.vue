<template>
  <footer class="footer">
    <div class="container">
      <div class="grid">
        <div class="col brand">
          <h3>&#127988; AK米欧</h3>
          <p>专注餐饮耗材采购的信息撮合平台<br/>不碰货、不碰钱，只做你的采购助手</p>
        </div>
        <div class="col">
          <h4>快速入口</h4>
          <a href="#how">服务流程</a>
          <a href="#submit">发布需求</a>
          <a href="#supplier">供应商入驻</a>
        </div>
        <div class="col">
          <h4>联系</h4>
          <p>邮箱：contact@akrmio.com</p>
        </div>
      </div>
      <div class="bottom">
        <p>&copy; 2026 AK米欧 akrmio.com · 信息中介平台，不参与交易</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer { background: #1a1a2e; color: #ccc; padding: 48px 0 24px; margin-top: 80px; }
.container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
.grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.col h3 { color: #fff; margin: 0 0 8px; font-size: 20px; }
.col h4 { color: #fff; margin: 0 0 12px; font-size: 14px; }
.col p { font-size: 14px; line-height: 1.8; color: #999; }
.col a { display: block; color: #aaa; text-decoration: none; margin-bottom: 8px; font-size: 14px; }
.col a:hover { color: #fff; text-decoration: none; }
.bottom { margin-top: 32px; padding-top: 16px; border-top: 1px solid #333; text-align: center; font-size: 13px; color: #666; }
@media (max-width: 640px) { .grid { grid-template-columns: 1fr; gap: 28px; } }
</style>