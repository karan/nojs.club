---
layout: default
title: "The NoJS Club!"
---

## The NoJS Club

<a href="https://twitter.com/intent/tweet?url=https%3A%2F%2Fnojs.club%2F&via=karangoel&text=Not%20all%20websites%20need%20Javascript%20to%20be%20beautiful%20and%20usable.%20This%20is%20a%20showcase%20of%20the%20Javascript-less%20web.&hashtags=noJSclub" target="_blank">Share on Twitter</a>

Not all websites need Javascript to be beautiful and usable. This is a showcase of the Javascript-less web.

**Why**

Developers have come to misuse, and at times abuse, Javascript to build modern websites. Pages are loading hundreds of KB of JS libraries to render some textual content.

Unnecessary Javascript <a href="https://httparchive.org/reports/page-weight#bytesJs" target="_blank">bloats websites</a>, <a href="https://modernweb.com/limit-javascript" target="_blank">hogs</a> system resources, enables <a href="https://www.wired.com/2015/11/i-turned-off-javascript-for-a-whole-week-and-it-was-glorious/" target="_blank">surveillance</a>, hinders <a href="https://www.deque.com/blog/current-design-trends-affect-web-accessibility/" target="_blank">accessibility</a> that's native to devices and clients, and introduces <a href="https://www.techrepublic.com/article/major-websites-plagued-by-lack-of-effective-security-against-javascript-vulnerabilities/" target="_blank">vulnerabilities</a>.

## How to join The Club

You can add your website to the list below by following these instructions:

1. Make sure there is no Javascript on your website. Look for any `<script>` tags on your page.
2. Do a [GTMetrix scan](https://gtmetrix.com/) on your website.
3. If your site satisfies this requirement, [submit an issue](https://github.com/karan/nojs.club/issues/new?assignees=&labels=&template=nojsrequest.md&title=example.com) on GitHub.
4. Once the request is approved, the domain will be added to the list below.

<ul class="members">
{% assign ordered_items = site.data.sites | sort: 'size' %}
{% for member in ordered_items %}
  <li>
    <span class="before" style="--data-size:{{ member.size }};"></span>
    <a href="https://{{ member.domain }}" target="_blank">
      {{ member.domain }}</a>
    <span class="after">{{ member.size | truncate: 5, "" }} KB</span>
  </li>
{% endfor %}
</ul>
