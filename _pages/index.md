---
layout: page
title: Home
id: home
permalink: /
---

# Welcome 가야고 정신병동 🏥

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  가야고 정신병원의 웹페이지의 로비이다.
  [[ㄱ계획에 대하여]]
</p>



<strong>최근 업데이트 목록들</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
