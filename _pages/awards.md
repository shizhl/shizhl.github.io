---
layout: page
permalink: /awards/
title: Awards
nav: true
nav_order: 3
description: Honors and awards
---


From 2019–2023 (B.E.) and 2023–2026 (M.S.), I was honored to receive the **Outstanding Academic Scholarship** (top 5%) from Shandong University every year. I am deeply grateful to everyone who has supported and helped me along the way.

Below are some selected distinctions I was fortunate to receive:

{% assign found_awards = false %}
<div class="cv">
  {% for entry in site.data.cv %}
    {% if entry.title == "Awards" and entry.contents and entry.contents.size > 0 %}
      {% assign found_awards = true %}
      <div class="card mt-3 p-3">
        {% include cv/time_table.html %}
      </div>
    {% endif %}
  {% endfor %}
</div>
{% unless found_awards %}
  <p>No awards listed.</p>
{% endunless %}

<!-- {% assign honors_entry = site.data.cv | where: "title", "Honors" | first %}
{% if honors_entry %}
<div class="cv">
  <div class="card mt-3 p-3">
    <h3 class="card-title font-weight-medium">{{ honors_entry.title }}</h3>
    {% include cv/time_table.html entry=honors_entry %}
  </div>
</div>
{% endif %} -->
