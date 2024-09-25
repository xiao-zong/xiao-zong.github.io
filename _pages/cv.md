---
layout: page
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}


# Education

* __Ph.D__ in Probability Theory, Aug 2017 -- Oct 2021, The University of Melbourne, Australia.
  * Under supervision of [Prof. Aihua Xia](https://researchers.ms.unimelb.edu.au/~aihuaxia@unimelb/)
* M.S. in Probability Theory and Mathematical Statistics, Sep 2015 -- Jun 2017, University of Science and Technology of China, China.
* B.S. in Mathematics and Applied Mathematics, Sep 2011 -- Jun 2015, Hunan University, China.

# Work experience

* Jul 2024 --  : Visiting Fellow
  * National University of Singapore

* Jan 2022 -- Jun 2024 : Research Fellow
  * Nanyang Technological University 
  * Supervisor: Prof. Nicolas Privault

* Sep 2021 -- Dec 2021 : Research Assistant
  * The University of Melbourne
  * Supervisor: Dr. Liuhua Peng

* 2018 -- 2021 : Casual Tutor
  * The University of Melbourne

# Publications

<!-- In Press Section -->
<h2>In Press</h2>
{% for publication in site.publications %}
  {% if publication.tags contains "InPress" %}
  <h3>{{ publication.title }}</h3>
  <p><strong>Authors:</strong> {{ publication.authors }}</p>
  <p>To be published in: <em>{{ publication.journal }}</em></p>
  <p><strong>Expected Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><strong>DOI:</strong> {{ publication.doi }}</p>
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
  <p>Published in: <em>{{ publication.journal }}</em></p>
  <p><strong>Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><strong>DOI:</strong> {{ publication.doi }}</p>
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
  <p>Presented at: <em>{{ publication.conference }}</em></p>
  <p><strong>Venue:</strong> {{ publication.venue }}</p>
  <p><strong>Year:</strong> {{ publication.date | date: "%Y" }}</p>
  <p><a href="{{ publication.link }}">Link to full text</a></p>
  {% if publication.doi %}
  <p><strong>DOI:</strong> {{ publication.doi }}</p>
  {% endif %}
  <hr>
  {% endif %}
{% endfor %}
  
# Talks

* NTU-Sorbonne Workshop, 19-21 February, 2024, Singapore.
* IMS Asia Pacific Rim Meeting 2024, 4-7 January, 2024, Melbourne, Australia. (Invited talk)
* Bernoulli-IMS One World Symposium 2020, 24-28 August, 2020, Online.
* 3rd Victorian Research Students’ Meeting in Probability and Statistics, 2 October, 2019, Melbourne, Australia.
* 20th INFORMS Applied Probability Society conference, 3-5 July, 2019, Brisbane, Australia.

## Teaching Experience

{% for teaching in site.teaching %}
  <h3>{{ teaching.title }}</h3>
  <p><strong>Institution:</strong> {{ teaching.institution }}</p>
  <p><strong>Position:</strong> {{ teaching.position }}</p>
  <p><strong>Dates:</strong> {{ teaching.date | date: "%Y" }}{% if teaching.end_date %} - {{ teaching.end_date | date: "%Y" }}{% endif %}</p>
  <p>{{ teaching.description }}</p>

  {{ teaching.content }} <!-- Display the detailed content of the teaching or tutorial experience -->

  <hr>
{% endfor %}
  
# Service and leadership

* Chairman, _Mathematical Modelling Association_
  * Hunan University, 2012 -- 2013
