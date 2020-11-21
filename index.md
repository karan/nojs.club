---
layout: default
title: "noJS.club!"
---

## noJS.club

You don't need Javascript to make a beautiful, usable web.

Javascript bloats websites, hogs system resources, enables surveillance, hinders accessibility, and introduces vulnerabilities.

You can add your website to the list below as long as it uses no Javascript. Just [open an issue](https://github.com/karan/nojs.club/issues) with the domain in the title.

<ul class="members">
{% assign ordered_items = site.data.sites | sort: 'size' %}
{% for member in ordered_items %}
  <li>
    <a href="https://{{ member.domain }}" target="_blank">
      {{ member.domain }}</a>
    <span class="after">{{ member.size | truncate: 4, "" }} kB</span>
  </li>
{% endfor %}
</ul>
