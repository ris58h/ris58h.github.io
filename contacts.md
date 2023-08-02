---
layout: page
title: Contacts
permalink: /contacts/
---

<ul class="contact-list">
  {%- if site.author -%}
  <li>{{ site.author | escape }}</li>
  {%- endif -%}
  {%- if site.email -%}
  <li><a href="mailto:{{ site.email }}">{{ site.email }}</a></li>
  {%- endif -%}
</ul>

{%- include social.html -%}
