---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

## Education

<ul class="timeline">
  <li class="timeline__item">
    <span class="timeline__date">2025 – present</span>
    <div>
      <span class="timeline__title">Ph.D. in Chemistry</span>
      <span class="timeline__meta">University of California, Riverside · Expected 2030</span>
    </div>
  </li>
  <li class="timeline__item">
    <span class="timeline__date">2025</span>
    <div>
      <span class="timeline__title">B.Pharm. in Pharmaceutical Science</span>
      <span class="timeline__meta">School of Medicine, The Chinese University of Hong Kong, Shenzhen</span>
    </div>
  </li>
</ul>

## Research Experience

<ul class="timeline">
  <li class="timeline__item">
    <span class="timeline__date">2025 – present</span>
    <div>
      <span class="timeline__title">Ph.D. Researcher, Wang Lab</span>
      <span class="timeline__meta">University of California, Riverside · Supervisor: Prof. Yinsheng Wang</span>
      <ul class="timeline__detail">
        <li>Chemical biology of RNA modifications and epitranscriptomics</li>
        <li>Computational tools for large-scale RNA biology and functional genomics data</li>
      </ul>
    </div>
  </li>
  <li class="timeline__item">
    <span class="timeline__date">Summer 2025</span>
    <div>
      <span class="timeline__title">Summer Research Intern, Yi Lab</span>
      <span class="timeline__meta">Peking University · Supervisor: Prof. Chengqi Yi</span>
      <ul class="timeline__detail">
        <li>Base editing</li>
      </ul>
    </div>
  </li>
  <li class="timeline__item">
    <span class="timeline__date">Winter 2023</span>
    <div>
      <span class="timeline__title">Undergraduate Research Assistant</span>
      <span class="timeline__meta">The Chinese University of Hong Kong, Shenzhen · Supervisor: Prof. Zhaoting Li</span>
      <ul class="timeline__detail">
        <li>Engineered bacteria for drug delivery and multiple cancer treatment</li>
        <li>Design and synthesis of an AIE probe for imaging biomolecular condensates</li>
      </ul>
    </div>
  </li>
  <li class="timeline__item">
    <span class="timeline__date">Summer 2023</span>
    <div>
      <span class="timeline__title">Research Intern</span>
      <span class="timeline__meta">Shenzhen Bay Laboratory · Supervisor: Dr. Mao Li</span>
      <ul class="timeline__detail">
        <li>Synthesis and characterization of a peptide-based biomimetic receptor</li>
      </ul>
    </div>
  </li>
  <li class="timeline__item">
    <span class="timeline__date">Fall 2020</span>
    <div>
      <span class="timeline__title">Undergraduate Research Assistant</span>
      <span class="timeline__meta">The Chinese University of Hong Kong, Shenzhen · Supervisor: Prof. Wing-Fu Lai</span>
      <ul class="timeline__detail">
        <li>Synthesis and characterization of polymer-based drug delivery systems</li>
      </ul>
    </div>
  </li>
</ul>

## Skills

<div class="skill-group">
  <h3>Molecular and Cell Biology</h3>
  <ul class="chips chips--accent">
    <li>Polysome profiling</li>
    <li>Cell culture</li>
    <li>Bacterial culture</li>
    <li>Western blot</li>
    <li>PCR</li>
    <li>SDS-PAGE</li>
    <li>Agarose gel electrophoresis</li>
    <li>ELISA</li>
    <li>Flow cytometry</li>
    <li>Confocal laser scanning microscopy</li>
  </ul>
</div>

<div class="skill-group">
  <h3>Computational</h3>
  <ul class="chips chips--accent">
    <li>Python</li>
    <li>PyTorch</li>
    <li>Structural modeling and molecular simulation</li>
    <li>Clinical data analysis</li>
    <li>NGS data analysis</li>
  </ul>
</div>

<div class="skill-group">
  <h3>Analytical Chemistry</h3>
  <ul class="chips">
    <li>Mass spectrometry</li>
    <li>HPLC (analytical and preparative)</li>
    <li>NMR</li>
    <li>FT-IR</li>
    <li>UV-Vis</li>
    <li>Fluorescence spectroscopy</li>
    <li>ITC</li>
    <li>DLS</li>
    <li>NTA</li>
    <li>SEM</li>
    <li>TEM</li>
    <li>TGA</li>
  </ul>
</div>

<div class="skill-group">
  <h3>Synthesis</h3>
  <ul class="chips">
    <li>Organic synthesis</li>
    <li>Solid-phase peptide synthesis</li>
    <li>Schlenk technique</li>
    <li>Column chromatography</li>
    <li>TLC</li>
    <li>Recrystallization</li>
  </ul>
</div>

## Publications

{% assign pubs = site.publications | sort: "date" | reverse %}
<ul class="pub-list">
  {% for pub in pubs %}
    {% include pub-item.html pub=pub %}
  {% endfor %}
</ul>

{% if site.data.manuscripts %}
<h3>Under Review and In Revision</h3>
{% include manuscript-list.html %}
{% endif %}

## Talks

{% assign talks = site.talks | sort: "date" | reverse %}
<ul class="timeline">
  {% for item in talks %}
    {% include timeline-item.html item=item %}
  {% endfor %}
</ul>

## Teaching

{% assign teaching = site.teaching | sort: "date" | reverse %}
<ul class="timeline">
  {% for item in teaching %}
    {% include timeline-item.html item=item %}
  {% endfor %}
</ul>

## Service

<ul class="timeline">
  <li class="timeline__item">
    <span class="timeline__date">Undergraduate</span>
    <div>
      <span class="timeline__title">New Media Center, Diligentia College</span>
      <span class="timeline__meta">Part-time work · The Chinese University of Hong Kong, Shenzhen</span>
    </div>
  </li>
</ul>
