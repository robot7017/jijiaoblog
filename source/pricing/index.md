---
title: 费用标准
date: 2025-12-05 00:00:00
---

<style>
/* 自定义费用表格样式，适配BlueLake主题 */
.pricing-table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
}
.pricing-table th, .pricing-table td {
  padding: 12px;
  text-align: left;
  border-bottom: 1px solid #eee;
}
.pricing-table th {
  background-color: #f5f5f5;
  font-weight: bold;
}
.grade-section {
  margin: 30px 0;
}
.grade-title {
  font-size: 1.5em;
  color: #333;
  margin-bottom: 15px;
}
</style>

# 家教辅导费用标准

以下是各年级、各科目一对一辅导的费用标准，具体价格可根据课时量和个性化需求适当调整：

<!-- 遍历配置中的费用数据 -->
{% for grade in config.tutoring.pricing %}
<div class="grade-section">
  <h2 class="grade-title">{{ grade.category }}</h2>
  <table class="pricing-table">
    <thead>
      <tr>
        <th>科目</th>
        <th>费用（元/小时）</th>
      </tr>
    </thead>
    <tbody>
      {% for subject in grade.subjects %}
      <tr>
        <td>{{ subject.name }}</td>
        <td>{{ subject.price }}</td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
{% endfor %}

<div style="margin-top: 30px; padding: 15px; background-color: #f9f9f9; border-left: 4px solid #42b983;">
  <strong>温馨提示：</strong><br>
  - 一次性购买20课时以上可享受9折优惠<br>
  - 老学员推荐新学员可获赠2课时<br>
  - 具体费用以咨询为准，可根据孩子情况定制套餐
</div>