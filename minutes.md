---
layout: default
title: Meeting Minutes
permalink: /minutes/
---

<div class="card">
  <h1>Meeting Minutes</h1>
  <p>Here you can find the minutes from our past meetings.</p>
  
  <ul>
    {% for minute in site.minutes %}
      <li><a href="{{ minute.url | relative_url }}">{{ minute.title }}</a></li>
    {% else %}
      <li><em>No minutes available yet.</em></li>
    {% endfor %}
  </ul>
  
  <p>
    <small>Older minutes are available in the archive.</small>
  </p>
</div>
