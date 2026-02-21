---
permalink: /
title: ""
layout: single
author_profile: true   # 如果你不想要左侧sidebar，把这里改成 false
---

## About Me {: #about}

I am Aoyu Liu, an undergraduate student at the [Yingcai Honors College](https://www.yingcai.uestc.edu.cn/en/),
[University of Electronic Science and Technology of China](https://en.uestc.edu.cn/), where I am pursuing a B.S. in Mathematics and Computer Science.

By the time of my sophomore year, my research focused on low-level computer vision.
I work under the guidance of [Prof. Shuaicheng Liu](https://liushuaicheng.org) in the
[Image Processing Lab](https://www.sice.uestc.edu.cn/kxyj/kytd/xxgcx/txclyjtd.htm) at UESTC.
During this period, I am fortunate to work closely with [Dr. Zhen Liu](https://liuzhen03.github.io/).

---

## News {: #news}

- **2026**: Our paper *ExpoCM: Exposure-Aware One-Step Generative Single-Image HDR Reconstruction* is accepted to **CVPR 2026**.

---

## Publications {: #publications}

{% assign pubs = site.publications | sort: "date" | reverse %}

{% for p in pubs %}
<div style="display:flex; gap:16px; align-items:flex-start; margin:18px 0;">

  {% if p.header.teaser %}
  <div style="flex:0 0 180px;">
    <img src="{{ '/images/' | append: p.header.teaser | relative_url }}"
         style="width:180px; height:auto; border-radius:10px;"
         alt="teaser">
  </div>
  {% endif %}

  <div style="flex:1;">
    <div style="font-size:1.05rem; font-weight:600; line-height:1.35;">
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
    </div>

    {% if p.authors %}
    <div style="margin-top:4px;">{{ p.authors }}</div>
    {% endif %}

    <div style="margin-top:4px; color:#666;">
      <i>{{ p.venue }}</i>, {{ p.date | date: "%Y" }}
    </div>

    <div style="margin-top:6px;">
      {% if p.paperurl %}<a href="{{ p.paperurl }}">Paper</a>{% endif %}
      {% if p.bibtexurl %} | <a href="{{ p.bibtexurl }}">BibTeX</a>{% endif %}
      {% if p.slidesurl %} | <a href="{{ p.slidesurl }}">Slides</a>{% endif %}
      {% if p.codeurl %} | <a href="{{ p.codeurl }}">Code</a>{% endif %}
    </div>
  </div>

</div>
{% endfor %}

---

## Co-authors {: #coauthors}

- [Zhen Liu](https://liuzhen03.github.io/)
- [Ziyi Wang](https://ziyiwang.me/)
- [Shuaicheng Liu](http://liushuaicheng.org/)