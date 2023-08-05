---
layout: default
# title: Home
---

<h2>Blog</h2>
{%- assign posts = site.posts | slice: 0, 3 -%}
{%- include posts.html posts=posts -%}
{%- if posts.size > 0 -%}
<p><a href="/blog/">View all posts</a></p>
{%- endif -%}

<h2>Projects</h2>
{%- assign projects = site.data.projects | slice: 0, 3 -%}
{%- include projects.html projects=projects -%}
{%- if projects.size > 0 -%}
<p><a href="/projects/">View all projects</a></p>
{%- endif -%}
