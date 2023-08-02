---
layout: default
title: Projects
permalink: /projects/
---

<div class="home">
  <!-- {%- if page.title -%}
    <h1 class="page-heading">{{ page.title }}</h1>
  {%- endif -%} -->

  <!-- {{ content }} -->

  <h2 class="post-list-heading">Projects</h2>
  <ul class="post-list">
      {%- for project in site.data.projects -%}
      <li>
      <h3>
          <a class="post-link" href="{{ project.url | absolute_url }}">
          {{ project.name | escape }}
          </a>
      </h3>
      {{ project.description | escape }}
      </li>
      {%- endfor -%}
  </ul>

</div>
