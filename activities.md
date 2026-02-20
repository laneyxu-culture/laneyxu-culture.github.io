---
layout: page
title: "Activities"
---

## 🎬 Latest Videos

<div style="margin: 30px 0;">
  <div style="max-width: 800px; margin: 0 auto 40px auto;">
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 12px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/eegzVC9ZKs8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"></iframe>
    </div>
    <p style="text-align: center; margin-top: 10px; color: #555; font-style: italic;">
      February 2026, invited to share the Chinese Spring Festival with kindergarteners at Nativity Catholic School in Indianapolis
    </p>
  </div>

  <div style="max-width: 800px; margin: 0 auto;">
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 12px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/aojqEZt33Ck" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"></iframe>
    </div>
    <p style="text-align: center; margin-top: 10px; color: #555; font-style: italic;">
      St. Francis High School Chinese New Year Fair 2026 Trailer
    </p>
  </div>
</div>

---

## 🖼️ Posters

<div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; margin: 30px 0;">
  {% for poster in site.posters %}
    <div style="text-align: center;">
      <img src="{{ poster.image }}" style="width:100%; border-radius:8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <p style="margin-top: 5px; color: #8B4513; font-weight: 500;">{{ poster.title }}</p>
      <p style="font-size: 0.85em; color: #666;">{{ poster.date | date: "%B %d, %Y" }}</p>
    </div>
  {% endfor %}
</div>

---

## 📸 Photos

### SFHS Chinese New Year Fair 2026

<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px;">
  <img src="/assets/img/activities/spring-1.jpg" style="width:100%; border-radius:8px;">
  <img src="/assets/img/activities/spring-2.jpg" style="width:100%; border-radius:8px;">
  <img src="/assets/img/activities/spring-3.jpg" style="width:100%; border-radius:8px;">
</div>

---

## 📄 Activity PPTs

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 25px; margin: 30px 0;">
  {% for ppt in site.ppt_files %}
    <div style="border: 1px solid #e0e0e0; padding: 15px; border-radius: 12px; background: #fafafa;">
      <h4 style="margin-top: 0; color: #8B4513; font-size: 1em;">{{ ppt.title }}</h4>
      <iframe src="/assets/pdfs/{{ ppt.file }}" width="100%" height="250" style="border: none; border-radius: 8px; background: #f0f0f0;"></iframe>
      <p style="margin-top: 10px; text-align: right;">
        <a href="/assets/pdfs/{{ ppt.file }}" target="_blank" style="color: #8B4513; text-decoration: none;">Open in new window ↗</a>
      </p>
    </div>
  {% endfor %}
</div>