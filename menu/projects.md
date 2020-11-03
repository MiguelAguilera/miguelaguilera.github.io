---
layout: page
title: Projects
---
<ul class="posts">
{% for project in site.projects %}
- {{ project.title }}
{% endfor %}

{% for post in site.posts %}
- {{ post.title }}
{% endfor %}
</ul>
<div class="posts">
  <h3>
    <a href="http://maguilera.net">Criticality, phase transitions and information integration for modelling autonomy and agency</a>
  </h3>
<!--  <div class="thumbnail-container">-->
    <a href="http://maguilera.net"><img src="{{ site.github.url }}/assets/img/project-agency-stat-phys.png"></a>
<!--  </div>-->
</div>
