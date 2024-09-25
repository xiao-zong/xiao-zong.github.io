---
layout: page
title: "Publications"
permalink: /publications/
---

# Publications

<!-- In Press Section -->
<h2>In Press</h2>
{% for publication in site.publications %}
  {% if publication.tags contains "InPress" %}
  <h3>{{ publication.title }}</h3>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p><em>To be published in:</em> {{ publication.journal }}</p>
  <p><strong>Expected Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><a href="{{ publication.doi }}">DOI: {{ publication.doi }}</a></p>
  {% endif %}
  <hr>
  {% endif %}
{% endfor %}

<!-- Journal Articles Section -->
<h2>Journal Articles</h2>
{% for publication in site.publications %}
  {% if publication.tags contains "Journal" %}
  <h3>{{ publication.title }}</h3>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p><em>Published in:</em> {{ publication.journal }}</p>
  <p><strong>Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><a href="{{ publication.doi }}">DOI: {{ publication.doi }}</a></p>
  {% endif %}
  <hr>
  {% endif %}
{% endfor %}

<!-- Conference Papers Section -->
<h2>Conference Papers</h2>
{% for publication in site.publications %}
  {% if publication.tags contains "Conference" %}
  <h3>{{ publication.title }}</h3>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p><em>Presented at:</em> {{ publication.conference }}</p>
  <p><strong>Venue:</strong> {{ publication.venue }}</p>
  <p><strong>Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><a href="{{ publication.doi }}">DOI: {{ publication.doi }}</a></p>
  {% endif %}
  <hr>
  {% endif %}
{% endfor %}
