---
title: 家长信息登记
date: 2025-12-05 00:00:00
---

<style>
/* 自定义表单容器样式 */
.registration-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.form-title {
  color: #333;
  margin-bottom: 10px;
}
.form-desc {
  color: #666;
  margin-bottom: 20px;
}
.form-iframe {
  width: 100%;
  height: 800px;
  border: none;
  border-radius: 4px;
}
.contact-info {
  margin-top: 30px;
  padding: 15px;
  background-color: #fff;
  border-left: 4px solid #42b983;
}
</style>

<div class="registration-container">
  <h1 class="form-title">{{ config.tutoring.registration.form_title }}</h1>
  <p class="form-desc">{{ config.tutoring.registration.form_desc }}</p>

  <!-- 嵌入腾讯文档表单（使用iframe） -->
  <iframe class="form-iframe" src="{{ config.tutoring.registration.form_url }}"></iframe>

  <div class="contact-info">
    <h3>其他联系方式</h3>
    <ul>
      <li>📞 联系电话：{{ config.tutoring.contact.phone }}</li>
      <li>📧 官方邮箱：{{ config.tutoring.contact.email }}</li>
      <li>📍 办公地址：{{ config.tutoring.contact.address }}</li>
      <li>💬 微信咨询：<img src="{{ config.tutoring.contact.wechat_qr }}" width="120" alt="微信二维码" style="margin-top: 10px;"></li>
    </ul>
  </div>
</div>