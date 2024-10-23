---
layout: page
title: Research
permalink: /research/
description: A collection of Wentao's research projects
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->

My research focus on the interaction between traditional spatial statistics and real world applications.

---

# Neural Networks for Geospatial Data



<div align="center">
<a href="https://www.tandfonline.com/doi/abs/10.1080/01621459.2024.2356293?casa_token=UaGsBumw4JAAAAAA:RD4cFpZW7lk3pu8Q5uVdxm5o3_RXWKRLXgxByEgl68qENKJfiNsS_Ci5izQ9WMQkZUKgSXasagyLQw">
  <img
    src="./assets/img/MISE_dim5_main.png"
    width="800">
</a>
</div>

---

# GeospaNN: a formal implementation of the Neural Networks for geospatial data

<div align="center">
<a href="https://www.tandfonline.com/doi/abs/10.1080/01621459.2024.2356293?casa_token=UaGsBumw4JAAAAAA:RD4cFpZW7lk3pu8Q5uVdxm5o3_RXWKRLXgxByEgl68qENKJfiNsS_Ci5izQ9WMQkZUKgSXasagyLQw">
  <img
    src="./assets/img/updated_NN_figure.png"
    width="800">
</a>
</div>



<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
