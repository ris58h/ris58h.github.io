---
layout: page
title: Blog
---

{%- assign posts = site.posts -%}
{%- if posts.size > 0 -%}
<ul class="post-list">
  {%- for post in posts -%}
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
{%- else -%}
<p>No posts yet.</p>
{%- endif -%}

<!-- <p class="rss-subscribe">
<svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#rss' | relative_url }}"></use></svg>
<a href="{{ "/blog/feed.xml" | relative_url }}">Feed</a>
</p> -->
