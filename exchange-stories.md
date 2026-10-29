---
layout: page
title: "Exchange Stories"
---

## 🏆 Holiday Video Contest 2024 Honorable Mention

<div style="max-width: 800px; margin: 30px auto;">
  <a href="https://www.youtube.com/watch?v=hrH0YLRcBr0" target="_blank" style="display: block; position: relative; border-radius: 12px; overflow: hidden; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
    <!-- 视频封面图 -->
    <img src="https://img.youtube.com/vi/hrH0YLRcBr0/maxresdefault.jpg" alt="Holiday Video Contest 2024" style="width: 100%; display: block;">
    <!-- 播放按钮 -->
    <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 68px; height: 48px; background: rgba(0,0,0,0.7); border-radius: 10px; display: flex; justify-content: center; align-items: center;">
      <div style="width: 0; height: 0; border-top: 10px solid transparent; border-bottom: 10px solid transparent; border-left: 16px solid white;"></div>
    </div>
  </a>
  <p style="text-align: center; margin-top: 15px; color: #555; font-style: italic;">
    Published by 2024 from the exchange year in Oregon.
  </p>
</div>

---

## 🎬 Spring Video Contest 2025 Winner

<div style="max-width: 800px; margin: 30px auto;">
  <a href="https://www.youtube.com/watch?v=BqIyJWg4gR4" target="_blank" style="display: block; position: relative; border-radius: 12px; overflow: hidden; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
    <!-- 视频封面图 -->
    <img src="https://img.youtube.com/vi/BqIyJWg4gR4/hqdefault.jpg" alt="Spring Video Contest 2025" style="width: 100%; display: block;">
    <!-- 播放按钮 -->
    <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 68px; height: 48px; background: rgba(0,0,0,0.7); border-radius: 10px; display: flex; justify-content: center; align-items: center;">
      <div style="width: 0; height: 0; border-top: 10px solid transparent; border-bottom: 10px solid transparent; border-left: 16px solid white;"></div>
    </div>
  </a>
  <p style="text-align: center; margin-top: 15px; color: #555; font-style: italic;">
    Published by 2025 from the exchange year in Oregon.
  </p>
</div>

---

## 📖 Stories from 303 Days

*303 days, 6 moments. Chinese original text, English machine-translated for reference only.*

{% assign stories = site.stories | sort: "order" %}
{% for s in stories %}
<div style="background:#fff; border:2px solid #B22222; border-radius:16px; padding:20px; margin:20px 0; box-shadow:0 4px 8px rgba(178,34,34,.1);">
  <a href="{{ s.url }}" style="text-decoration:none; color:inherit;">
    <h3 style="color:#B22222; margin:0 0 6px 0;">{{ s.title }}</h3>
    <p style="color:#777; margin:4px 0; font-size:0.9em;">{{ s.date | date: "%Y-%m-%d" }}</p>
    {% if s.title_en %}<p style="color:#999; font-style:italic; margin:4px 0 0 0;">{{ s.title_en }}</p>{% endif %}
  </a>
</div>
{% endfor %}