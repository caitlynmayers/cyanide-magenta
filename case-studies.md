---
layout: page
title: Case Studies
---

<div id="home">
  <h1>Test - Case Studies</h1>
  <ul class="posts">
    {% for case-study in site.case-studies %}
      <li><a href="{{ case-study.url }}">{{ case-study.title }}</a></li>
    {% endfor %}
  </ul>
</div>
