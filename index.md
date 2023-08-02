---
layout: page
title: Home
---

<h2>Blog</h2>
<ul class="post-list">
  {%- for post in site.posts limit:3 -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endfor -%}
</ul>
<a href="/blog/">View all posts</a>

<h2>Projects</h2>
<ul class="post-list">
    {%- for project in site.data.projects limit:3 -%}
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
<a href="/projects/">View all projects</a>
