---
layout: page
title: "Publications"
permalink: /publications/
---

# Publications

## Journal Articles
{% for publication in site.publications %}
  {% if publication.tags contains "Journal" %}
  - **{{ publication.title }}**  
    *{{ publication.authors }}*  
    Published in: *{{ publication.journal }}*  
    **Year**: {{ publication.date | date: "%Y" }}  
    [Link to full text]({{ publication.link }})
    {% if publication.doi %}  
    [DOI: {{ publication.doi }}]({{ publication.doi }})
    {% endif %}
  ---
  {% endif %}
{% endfor %}

## Conference Papers
{% for publication in site.publications %}
  {% if publication.tags contains "Conference" %}
  - **{{ publication.title }}**  
    *{{ publication.authors }}*  
    Presented at: *{{ publication.conference }}*  
    **Venue**: {{ publication.venue }}  
    **Year**: {{ publication.date | date: "%Y" }}  
    [Link to full text]({{ publication.link }})
    {% if publication.doi %}  
    [DOI: {{ publication.doi }}]({{ publication.doi }})
    {% endif %}
  ---
  {% endif %}
{% endfor %}

## In Press
{% for publication in site.publications %}
  {% if publication.tags contains "InPress" %}
  - **{{ publication.title }}**  
    *{{ publication.authors }}*  
    To be published in: *{{ publication.journal }}*  
    **Expected Year**: {{ publication.date | date: "%Y" }}  
    [Link to full text]({{ publication.link }})
  ---
  {% endif %}
{% endfor %}
