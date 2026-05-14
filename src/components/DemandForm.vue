<template>
  <div class="form-wrapper">
    <form @submit.prevent="handleSubmit" class="demand-form">
      <div class="field">
        <label>采购品类 <span class="req">*</span></label>
        <select v-model="form.category" required>
          <option value="" disabled>请选择品类</option>
          <option>一次性餐具（打包盒、筷子、吸管）</option>
          <option>纸制品（纸杯、纸巾、打包袋）</option>
          <option>清洁用品（洗洁精、消毒液）</option>
          <option>厨房设备（冷柜、灶具、排烟）</option>
          <option>定制用品（Logo纸杯、定制餐盒）</option>
          <option>门头招牌 / 装修工程</option>
          <option>其他</option>
        </select>
      </div>
      <div class="field">
        <label>预计采购数量 <span class="req">*</span></label>
        <input type="text" v-model="form.quantity" placeholder="例如：500个 / 100箱 / 按需" required />
      </div>
      <div class="field">
        <label>规格要求</label>
        <textarea v-model="form.spec" rows="3" placeholder="尺寸、材质、颜色等要求（选填）"></textarea>
      </div>
      <div class="field">
        <label>所在城市 <span class="req">*</span></label>
        <input type="text" v-model="form.city" placeholder="例如：上海 / 广州" required />
      </div>
      <div class="field">
        <label>预算范围 <span class="req">*</span></label>
        <select v-model="form.budget" required>
          <option value="" disabled>请选择</option>
          <option>1,000元以下</option>
          <option>1,000 - 5,000元</option>
          <option>5,000 - 20,000元</option>
          <option>20,000 - 100,000元</option>
          <option>10万元以上</option>
          <option>先询价看看</option>
        </select>
      </div>
      <div class="field">
        <label>手机号 <span class="req">*</span></label>
        <input type="tel" v-model="form.phone" placeholder="用于供应商联系您" required maxlength="11" />
        <p class="field-hint">提交后将发送短信验证码验证</p>
      </div>
      <button type="submit" class="btn btn-primary btn-lg submit-btn" :disabled="submitting">
        {{ submitting ? '提交中...' : '提交需求，匹配工厂' }}
      </button>
      <p class="form-footnote">&#128481; 提交后最多5家工厂联系您 · 您的电话不会对外公开</p>
    </form>

    <div v-if="submitted" class="success-card">
      <div class="success-icon">&#9989;</div>
      <h3>需求提交成功！</h3>
      <p>系统正在匹配合适的供应商，<br/>符合条件的工厂会尽快联系您。</p>
      <button class="btn btn-outline" @click="resetForm">再发一个需求</button>
    </div>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'
const submitting = ref(false)
const submitted = ref(false)
const form = reactive({ category: '', quantity: '', spec: '', city: '', budget: '', phone: '' })
async function handleSubmit() {
  submitting.value = true
  await new Promise(r => setTimeout(r, 1500))
  submitting.value = false
  submitted.value = true
}
function resetForm() {
  form.category = ''; form.quantity = ''; form.spec = ''; form.city = ''; form.budget = ''; form.phone = ''
  submitted.value = false
}
</script>

<style scoped>
.form-wrapper { max-width: 600px; margin: 0 auto; position: relative; }
.demand-form { background: #f8f9fa; padding: 40px; border-radius: 16px; border: 1px solid #eee; }
.field { margin-bottom: 20px; }
.field label { display: block; font-size: 14px; font-weight: 600; margin-bottom: 6px; color: #333; }
.req { color: #e74c3c; }
.field select, .field input, .field textarea { width: 100%; padding: 12px 16px; border: 1px solid #ddd; border-radius: 8px; font-size: 15px; background: #fff; transition: border-color 0.2s; font-family: inherit; }
.field select:focus, .field input:focus, .field textarea:focus { outline: none; border-color: #e74c3c; box-shadow: 0 0 0 3px rgba(231,76,60,0.1); }
.field-hint { font-size: 12px; color: #999; margin-top: 4px; }
.submit-btn { width: 100%; margin-top: 8px; }
.submit-btn:disabled { opacity: 0.6; cursor: not-allowed; }
.form-footnote { text-align: center; font-size: 13px; color: #888; margin-top: 16px; }
.success-card { position: absolute; inset: 0; background: #fff; display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 40px; border-radius: 16px; border: 2px solid #27ae60; text-align: center; }
.success-icon { font-size: 56px; margin-bottom: 16px; }
.success-card h3 { font-size: 22px; color: #27ae60; margin-bottom: 12px; }
.success-card p { color: #666; line-height: 1.8; margin-bottom: 24px; }
@media (max-width: 640px) { .demand-form { padding: 24px; } }
</style>