---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
<div class="wordwrap">
  You can also find my articles on 
  <a href="https://scholar.google.com/citations?user=en_NRKkAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener">
    my Google Scholar profile
  </a>.
</div>
{% endif %}

{% include base_path %}

{% comment %}
--------------------------------------------
Assign publication groups (sorted by date)
--------------------------------------------
{% endcomment %}
{% assign inpress = site.publications | where_exp: "item", "item.tags contains 'InPress'" | sort: "date" | reverse %}
{% assign journals = site.publications | where_exp: "item", "item.tags contains 'Journal'" | sort: "date" | reverse %}
{% assign conferences = site.publications | where_exp: "item", "item.tags contains 'Conference'" | sort: "date" | reverse %}

---

## In Press
{% if inpress.size > 0 %}
  {% for publication in inpress %}
    {% include publication-entry.html publication=publication %}
  {% endfor %}
{% else %}
  <p>No in-press articles at the moment.</p>
{% endif %}

---

## Journal Articles
{% if journals.size > 0 %}
  {% for publication in journals %}
    {% include publication-entry.html publication=publication %}
  {% endfor %}
{% else %}
  <p>No journal publications available.</p>
{% endif %}

---

## Conference Papers
{% if conferences.size > 0 %}
  {% for publication in conferences %}
    {% include publication-entry.html publication=publication %}
  {% endfor %}
{% else %}
  <p>No conference papers available.</p>
{% endif %}

---

{% comment %}
--------------------------------------------
Optional: Show all publications (legacy style)
--------------------------------------------
{% endcomment %}
### All Publications
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
