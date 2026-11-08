---
layout: page
title: "Activities"
---

## 🎬 Latest Videos

<div style="margin: 30px 0;">
  <div style="max-width: 800px; margin: 0 auto 40px auto;">
    <a href="https://www.youtube.com/watch?v=eegzVC9ZKs8" target="_blank" style="display: block; position: relative; border-radius: 12px; overflow: hidden; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <img src="https://img.youtube.com/vi/eegzVC9ZKs8/maxresdefault.jpg" alt="Video thumbnail" style="width: 100%; display: block;">
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 68px; height: 48px; background: rgba(0,0,0,0.7); border-radius: 10px; display: flex; justify-content: center; align-items: center;">
        <div style="width: 0; height: 0; border-top: 10px solid transparent; border-bottom: 10px solid transparent; border-left: 16px solid white;"></div>
      </div>
    </a>
    <p style="text-align: center; margin-top: 10px; color: #555; font-style: italic;">
      February 2026, invited to share the Chinese Spring Festival with kindergarteners at Nativity Catholic School in Indianapolis
    </p>
  </div>

  <div style="max-width: 800px; margin: 0 auto;">
    <a href="https://www.youtube.com/watch?v=aojqEZt33Ck" target="_blank" style="display: block; position: relative; border-radius: 12px; overflow: hidden; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <img src="https://img.youtube.com/vi/aojqEZt33Ck/maxresdefault.jpg" alt="Video thumbnail" style="width: 100%; display: block;">
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 68px; height: 48px; background: rgba(0,0,0,0.7); border-radius: 10px; display: flex; justify-content: center; align-items: center;">
        <div style="width: 0; height: 0; border-top: 10px solid transparent; border-bottom: 10px solid transparent; border-left: 16px solid white;"></div>
      </div>
    </a>
    <p style="text-align: center; margin-top: 10px; color: #555; font-style: italic;">
      St. Francis High School Chinese New Year Fair 2026 Trailer
    </p>
  </div>
</div>

---

<!-- 标签栏导航 -->
<div style="display: flex; gap: 10px; margin: 30px 0; border-bottom: 2px solid #B22222; padding-bottom: 10px; flex-wrap: wrap;">
  <button onclick="showTab('posters')" style="background: #B22222; color: white; border: none; padding: 10px 25px; border-radius: 25px; cursor: pointer; font-weight: 500; font-size: 1em;">📋 Posters</button>
  <button onclick="showTab('photos')" style="background: #f0f0f0; color: #B22222; border: none; padding: 10px 25px; border-radius: 25px; cursor: pointer; font-weight: 500; font-size: 1em;">📸 Photos</button>
  <button onclick="showTab('ppts')" style="background: #f0f0f0; color: #B22222; border: none; padding: 10px 25px; border-radius: 25px; cursor: pointer; font-weight: 500; font-size: 1em;">📄 Activity PPTs</button>
  
  <!-- 新增的导航按钮 -->
  <button onclick="showTab('festivals')" style="background: #f0f0f0; color: #B22222; border: none; padding: 10px 25px; border-radius: 25px; cursor: pointer; font-weight: 500; font-size: 1em;">🏮 Chinese Festivals</button>
  <button onclick="showTab('solar_terms')" style="background: #f0f0f0; color: #B22222; border: none; padding: 10px 25px; border-radius: 25px; cursor: pointer; font-weight: 500; font-size: 1em;">🌿 Solar Terms</button>
</div>

<!-- Posters 内容区域 -->
<div id="posters" class="tab-content">
  <div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; margin: 20px 0;">
    {% for poster in site.posters %}
      <div style="text-align: center;">
        <img src="{{ poster.image }}" style="width:100%; border-radius:8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
        <p style="margin-top: 5px; color: #8B4513; font-weight: 500;">{{ poster.title }}</p>
        <p style="font-size: 0.85em; color: #666;">{{ poster.date | date: "%B %d, %Y" }}</p>
      </div>
    {% endfor %}
  </div>
</div>

<!-- Photos 内容区域 -->
<div id="photos" class="tab-content" style="display: none;">
  {% for album in site.photo_albums %}
    <div style="margin: 40px 0;">
      <h3 style="color: #B22222;">{{ album.title }}</h3>
      <p style="color: #666; margin-bottom: 20px;">{{ album.description }}</p>
      
      {% if album.status == "coming soon" %}
        <div style="background: #FFF5F0; padding: 30px; text-align: center; border-radius: 12px; border: 1px dashed #B22222;">
          <p style="color: #B22222; font-style: italic;">📸 Photos coming soon</p>
        </div>
      {% else %}
        <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px;">
          {% for photo in album.photos %}
            <img src="{{ photo }}" style="width:100%; border-radius:8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
          {% endfor %}
        </div>
      {% endif %}
    </div>
  {% endfor %}
</div>

<!-- PPTs 内容区域 -->
<div id="ppts" class="tab-content" style="display: none;">
  <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 25px; margin: 20px 0;">
    {% for ppt in site.ppt_files %}
      <div style="border: 1px solid #e0e0e0; padding: 15px; border-radius: 12px; background: #fafafa;">
        <h4 style="margin-top: 0; color: #8B4513; font-size: 1em;">{{ ppt.title }}</h4>
        <iframe src="/assets/pdfs/{{ ppt.file }}" width="100%" height="200" style="border: none; border-radius: 8px; background: #f0f0f0;"></iframe>
        <p style="margin-top: 10px; text-align: right;">
          <a href="/assets/pdfs/{{ ppt.file }}" target="_blank" style="color: #8B4513; text-decoration: none;">Open in new window ↗</a>
        </p>
      </div>
    {% endfor %}
  </div>
</div>

<!-- ================= 新增内容区域 ================= -->

<!-- Chinese Festivals 内容区域 (共 16 张图片) -->
<div id="festivals" class="tab-content" style="display: none;">
  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin: 20px 0;">
    
    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/01chuxi.jpg" alt="Chinese New Year's Eve" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Chinese New Year's Eve (除夕)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/02chuyi.jpg" alt="Chinese New Year's Day" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Chinese New Year's Day (初一)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/03chuer.jpg" alt="Second Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Second Day of CNY (初二)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/04chusan.jpg" alt="Third Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Third Day of CNY (初三)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/05chusi.jpg" alt="Fourth Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Fourth Day of CNY (初四)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/06chuwu.jpg" alt="Fifth Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Fifth Day of CNY (初五)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/07chuliu.jpg" alt="Sixth Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Sixth Day of CNY (初六)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/08chuqi.jpg" alt="Seventh Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Seventh Day of CNY (初七)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/09chuba.jpg" alt="Eighth Day of CNY" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Eighth Day of CNY (初八)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/10yuanxiao.jpg" alt="Lantern Festival" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Lantern Festival (元宵节)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/chongyang.jpg" alt="Double Ninth Festival" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Double Ninth Festival (重阳节)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/duanwu.jpg" alt="Dragon Boat Festival" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Dragon Boat Festival (端午节)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/guoqing.jpg" alt="National Day" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">National Day (国庆节)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/qixi.jpg" alt="Qixi Festival" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Qixi Festival (七夕节)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/yuandan.jpg" alt="New Year's Day" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">New Year's Day (元旦)</p>
    </div>

    <div style="text-align: center;">
      <img src="/assets/img/activities/festivals/zhongqiu.jpg" alt="Mid-Autumn Festival" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500;">Mid-Autumn Festival (中秋节)</p>
    </div>

  </div>
</div>

<!-- Solar Terms 内容区域 (共 15 张图片) -->
<div id="solar_terms" class="tab-content" style="display: none;">
  <div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; margin: 20px 0;">
    
    <!-- 11. 立春 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/11lichun.jpg" alt="Start of Spring" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Start of Spring (立春)</p>
    </div>

    <!-- 12. 雨水 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/12yushui.jpg" alt="Rain Water" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Rain Water (雨水)</p>
    </div>

    <!-- 13. 夏至 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/13xiazhi.jpg" alt="Summer Solstice" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Summer Solstice (夏至)</p>
    </div>

    <!-- 14. 小暑 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/14xiaoshu.jpg" alt="Minor Heat" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Minor Heat (小暑)</p>
    </div>

    <!-- 15. 大暑 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/15dashu.jpg" alt="Major Heat" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Major Heat (大暑)</p>
    </div>

    <!-- 16. 立秋 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/16liqiu.jpg" alt="Start of Autumn" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Start of Autumn (立秋)</p>
    </div>

    <!-- 17. 秋分 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/17qiufen.jpg" alt="Autumn Equinox" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Autumn Equinox (秋分)</p>
    </div>

    <!-- 18. 处暑 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/18chushu.jpg" alt="End of Heat" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">End of Heat (处暑)</p>
    </div>

    <!-- 19. 白露 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/19bailu.jpg" alt="White Dew" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">White Dew (白露)</p>
    </div>

    <!-- 20. 寒露 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/20hanlu.jpg" alt="Cold Dew" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Cold Dew (寒露)</p>
    </div>

    <!-- 21. 霜降 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/21shuangjiang.jpg" alt="Frost's Descent" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Frost's Descent (霜降)</p>
    </div>

    <!-- 22. 立冬 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/22lidong.jpg" alt="Start of Winter" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Start of Winter (立冬)</p>
    </div>

    <!-- 23. 小雪 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/23xiaoxue.jpg" alt="Minor Snow" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Minor Snow (小雪)</p>
    </div>

    <!-- 24. 小寒 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/24xiaohan.jpg" alt="Minor Cold" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Minor Cold (小寒)</p>
    </div>

    <!-- 25. 大寒 -->
    <div style="text-align: center;">
      <img src="/assets/img/activities/solar-terms/25dahan.jpg" alt="Major Cold" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 10px; color: #8B4513; font-weight: 500; font-size: 0.9em;">Major Cold (大寒)</p>
    </div>

  </div>
</div>

<!-- ================= 新增内容区域结束 ================= -->


<!-- 切换标签的JavaScript -->
<script>
function showTab(tabName) {
  // 隐藏所有内容区域
  var tabs = document.getElementsByClassName('tab-content');
  for (var i = 0; i < tabs.length; i++) {
    tabs[i].style.display = 'none';
  }
  
  // 显示选中的内容区域
  document.getElementById(tabName).style.display = 'block';
  
  // 更新按钮样式
  var buttons = document.querySelectorAll('button');
  for (var i = 0; i < buttons.length; i++) {
    buttons[i].style.background = '#f0f0f0';
    buttons[i].style.color = '#B22222';
  }
  
  // 高亮当前按钮
  event.target.style.background = '#B22222';
  event.target.style.color = 'white';
}
</script>