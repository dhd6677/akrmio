<template>
  <header class="header">
    <div class="container">
      <a href="/" class="logo">
        <span class="logo-icon">&#127988;</span>
        <span class="logo-text">AK米欧</span>
        <span class="logo-tag">餐饮耗材直采</span>
      </a>
      <nav class="nav">
        <a href="#how">服务流程</a>
        <a href="#submit" class="nav-cta">发布需求</a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header { background: #fff; border-bottom: 1px solid #eee; position: sticky; top: 0; z-index: 100; }
.container { max-width: 1200px; margin: 0 auto; padding: 0 24px; display: flex; justify-content: space-between; align-items: center; height: 64px; }
.logo { text-decoration: none; display: flex; align-items: center; gap: 8px; }
.logo:hover { text-decoration: none; }
.logo-icon { font-size: 24px; }
.logo-text { font-size: 22px; font-weight: 800; color: #e74c3c; }
.logo-tag { font-size: 12px; color: #999; }
.nav { display: flex; align-items: center; gap: 28px; }
.nav a { color: #333; text-decoration: none; font-size: 14px; transition: color 0.2s; }
.nav a:hover { color: #e74c3c; text-decoration: none; }
.nav-cta { background: #e74c3c; color: #fff !important; padding: 8px 20px; border-radius: 6px; font-weight: 600; }
.nav-cta:hover { background: #c0392b !important; }
@media (max-width: 640px) { .logo-tag { display: none; } .nav { gap: 16px; } }
</style>