<template>
  <div class="home">
    <section class="hero">
      <div class="container">
        <h1 class="hero-title">餐饮耗材采购<br/><span class="highlight">跳过中间商直连工厂</span></h1>
        <p class="hero-desc">发布采购需求，系统自动匹配合适的源头工厂。<br/>买方永久免费，不抽成、不竞价排名。</p>
        <div class="hero-actions">
          <a href="#submit" class="btn btn-primary btn-lg">立即发布需求</a>
          <a href="#how" class="btn btn-outline btn-lg">了解详情</a>
        </div>
        <div class="hero-stats">
          <div class="stat"><span class="num">100+</span><span class="lbl">源头工厂</span></div>
          <div class="stat"><span class="num">0</span><span class="lbl">平台抽成</span></div>
          <div class="stat"><span class="num">&le;5家</span><span class="lbl">最多联系</span></div>
        </div>
      </div>
    </section>

    <section class="steps" id="how">
      <div class="container">
        <h2 class="section-title">三步搞定采购</h2>
        <p class="section-sub">简单透明，60秒上手</p>
        <div class="steps-grid">
          <div class="step-card"><div class="step-num">01</div><h3>发布需求</h3><p>填写品类、数量、预算<br/>无需注册，全程免费</p></div>
          <div class="step-arrow">&rarr;</div>
          <div class="step-card"><div class="step-num">02</div><h3>系统匹配</h3><p>N+N算法智能推荐<br/>源头工厂+本地服务商</p></div>
          <div class="step-arrow">&rarr;</div>
          <div class="step-card"><div class="step-num">03</div><h3>工厂报价</h3><p>最多5家联系你<br/>比价选最优</p></div>
        </div>
      </div>
    </section>

    <section class="features">
      <div class="container">
        <h2 class="section-title">为什么选AK米欧</h2>
        <p class="section-sub">餐饮老板和供应商都信任的平台</p>
        <div class="features-grid">
          <div class="card"><div class="card-icon">&#128269;</div><h3>源头直连</h3><p>跳过中间商，直接从工厂拿价</p></div>
          <div class="card"><div class="card-icon">&#129302;</div><h3>智能匹配</h3><p>按品类、地区精准推送供应商</p></div>
          <div class="card"><div class="card-icon">&#128481;</div><h3>体验可控</h3><p>每单最多5家联系，不被骚扰</p></div>
          <div class="card"><div class="card-icon">&#128142;</div><h3>永久免费</h3><p>买方永不收费，不抽成不竞价</p></div>
        </div>
      </div>
    </section>

    <section class="form-section" id="submit">
      <div class="container">
        <h2 class="section-title">发布采购需求</h2>
        <p class="section-sub">填写下方信息，系统自动匹配源头工厂</p>
        <DemandForm />
      </div>
    </section>
  </div>
</template>

<script setup>
import DemandForm from '../components/DemandForm.vue'
</script>

<style scoped>
.hero { background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%); color: #fff; padding: 100px 0 80px; text-align: center; }
.hero-title { font-size: 42px; font-weight: 800; line-height: 1.3; margin-bottom: 20px; }
.hero-title .highlight { color: #e74c3c; }
.hero-desc { font-size: 18px; color: #aaa; margin-bottom: 36px; line-height: 1.8; }
.hero-actions { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }
.hero-stats { display: flex; justify-content: center; gap: 60px; margin-top: 60px; }
.stat { text-align: center; }
.stat .num { display: block; font-size: 28px; font-weight: 700; color: #e74c3c; }
.stat .lbl { display: block; font-size: 14px; color: #888; margin-top: 4px; }
.steps { padding: 80px 0; background: #fff; }
.steps-grid { display: flex; align-items: center; justify-content: center; gap: 12px; flex-wrap: wrap; }
.step-card { text-align: center; flex: 1; min-width: 200px; max-width: 280px; padding: 32px 20px; }
.step-num { font-size: 36px; font-weight: 800; color: #e74c3c; opacity: 0.6; margin-bottom: 12px; }
.step-card h3 { font-size: 18px; margin-bottom: 8px; color: #1a1a2e; }
.step-card p { color: #666; font-size: 14px; line-height: 1.7; }
.step-arrow { font-size: 28px; color: #ddd; }
.features { padding: 80px 0; background: #f8f9fa; }
.features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 24px; }
.card { background: #fff; padding: 36px 24px; border-radius: 12px; text-align: center; box-shadow: 0 2px 8px rgba(0,0,0,0.06); }
.card-icon { font-size: 42px; margin-bottom: 16px; }
.card h3 { font-size: 18px; margin-bottom: 8px; color: #1a1a2e; }
.card p { color: #666; font-size: 14px; }
.form-section { padding: 80px 0; background: #fff; }
@media (max-width: 768px) {
  .hero-title { font-size: 28px; } .hero-stats { gap: 30px; flex-wrap: wrap; }
  .steps-grid { flex-direction: column; } .step-arrow { transform: rotate(90deg); }
}
</style>