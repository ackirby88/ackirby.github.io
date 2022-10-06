---
layout: page
title: research
permalink: /projects/
description: My research focuses on the develop of computational simulation and data analysis tools to gain insight into fluid mechanics in the context of aerospace and wind energy applications. The underpinnings of my research are the Computional Fluid Dynamics codes I've developed over the past decade, in particular WAKE3D/dg4est, resulting in the highest fidelity wind farm and rotorcraft simulations to date. My long-term research goals are to develop multiscale high-order numerical methods applicable to renewable energy and aerospace communities on computing capabilities ranging from a single workstation all the way up to leadership-class heterogeneous exascale supercomputers. To achieve these goals, innovations in applied mathematics, computer science, and fluid dynamics are a must!
nav: true
nav_order: 1
display_categories: [Wind Energy, Fixed-Wing Aero, Rotorcraft Aero, Acoustics, Computing]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
