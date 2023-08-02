---
layout: page
title: Home
---

<h2>Blog</h2>
{%- assign top_posts = site.posts | slice: 0, 3 -%}
{%- if top_posts.size > 0 -%}
<ul class="post-list">
  {%- for post in top_posts -%}
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
<p><a href="/blog/">View all posts</a></p>
{%- else -%}
<p>No posts yet.<p>
{%- endif -%}

<h2>Projects</h2>
{%- assign top_projects = site.data.projects | slice: 0, 3 -%}
{%- if top_projects.size > 0 -%}
<ul class="post-list">
    {%- for project in top_projects -%}
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
<p><a href="/projects/">View all projects</a></p>
{%- else -%}
<p>No projects yet.<p>
{%- endif -%}
