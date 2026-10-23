---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p class="home-tagline">Epitranscriptomics · AI for biology</p>

I'm Shuyang Zhao (you can also call me Noah), a second-year Ph.D. student in Chemistry at the University of California, Riverside, working in [Prof. Yinsheng Wang's lab](https://wanglab.ucr.edu). I study the chemical biology of RNA modifications and build computational tools that make large biological datasets easier to process and compare.

Before coming to Riverside, I earned a B.Pharm. in Pharmaceutical Science from the School of Medicine at [The Chinese University of Hong Kong, Shenzhen](https://cuhk.edu.cn), with training in drug delivery, immunotherapy, organic chemistry and analytical chemistry. Along the way I worked on biomaterials and drug delivery with [Prof. Zhaoting Li](https://zhaotingli.com) and [Prof. Wing-Fu Lai](https://environment.leeds.ac.uk/faculty/staff/11935/dr-wing-fu-lai) at CUHK-Shenzhen, on chemical biology and peptide chemistry with [Dr. Mao Li](https://www.x-mol.com/groups/limao) at Shenzhen Bay Laboratory, and, in the summer of 2025, on genome editing with [Prof. Chengqi Yi](https://www.yilab.org.cn) at Peking University. I am grateful to each of them for their guidance.

If you are also interested in RNA modifications or computational tools for biology, feel free to write to me at shuyang.zhao[at]email.ucr.edu.

## Research interests

<div class="interest-grid">
  <div class="interest-card">
    <h3>Epitranscriptomics</h3>
    <p>The chemical biology of RNA modifications and of the enzymes that write, read and erase them.</p>
  </div>
  <div class="interest-card">
    <h3>AI for Biology</h3>
    <p>Computational pipelines and models for large biological datasets, from sequencing data to functional genomics screens.</p>
  </div>
</div>

## News

<ul class="news-list">
{% for item in site.data.news %}
  <li><span class="news-list__date">{{ item.date }}</span><span>{{ item.text }}</span></li>
{% endfor %}
</ul>

{% assign projects = site.projects | sort: "date" | reverse %}
{% if projects.size > 0 %}
## Projects

<div class="featured-projects">
{% for project in projects limit: 2 %}
  <a class="featured-project" href="{{ project.url | relative_url }}">
    {% if project.image %}<img src="{{ project.image | prepend: '/images/' | relative_url }}" alt="" loading="lazy">{% endif %}
    <div class="featured-project__body">
      <h3>{{ project.title | split: ":" | first }}</h3>
      <span>{{ project.title | split: ": " | last }}</span>
    </div>
  </a>
{% endfor %}
</div>
{% endif %}
