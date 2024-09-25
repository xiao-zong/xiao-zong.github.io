---
layout: page
title: "Publications"
permalink: /publications/
---

{% for publication in site.publications %}
  ### {{ publication.title }}

  **Authors**: {{ publication.authors }}

  {% if publication.tags contains "Journal" %}
  **Published in**: {{ publication.journal }}
  {% elsif publication.tags contains "Conference" %}
  **Presented at**: {{ publication.conference }}  
  **Venue**: {{ publication.venue }}
  {% endif %}

  **Date**: {{ publication.date | date: "%Y" }}  
  [Link to full text]({{ publication.link }})

  ---
{% endfor %}

