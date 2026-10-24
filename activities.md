---
layout: page
title: "Activities"
---

## 🎬 Latest Videos

<div style="margin: 30px 0;">
  <div style="max-width: 800px; margin: 0 auto 40px auto;">
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 12px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <iframe 
        src="https://www.youtube-nocookie.com/embed/eegzVC9ZKs8" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
        referrerpolicy="strict-origin-when-cross-origin" 
        allowfullscreen 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;">
      </iframe>
    </div>
    <p style="text-align: center; margin-top: 10px; color: #555; font-style: italic;">
      February 2026, invited to share the Chinese Spring Festival with kindergarteners at Nativity Catholic School in Indianapolis
    </p>
  </div>

  <div style="max-width: 800px; margin: 0 auto;">
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 12px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <iframe 
        src="https://www.youtube-nocookie.com/embed/aojqEZt33Ck" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
        referrerpolicy="strict-origin-when-cross-origin" 
        allowfullscreen 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;">
      </iframe>
    </div>
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