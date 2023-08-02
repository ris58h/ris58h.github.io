---
layout: page
title: Projects
---

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
