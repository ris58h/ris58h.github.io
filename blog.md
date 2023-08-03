---
layout: page
title: Blog
---

<ul class="post-list">
  {%- for post in site.posts -%}
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

<!-- <p class="rss-subscribe">
<svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#rss' | relative_url }}"></use></svg>
<a href="{{ "/blog/feed.xml" | relative_url }}">Feed</a>
</p> -->
