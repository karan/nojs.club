# noJS.club

You don't need Javascript to make a beautiful, usable web.

Javascript bloats websites, hogs system resources, enables surveillance, hinders accessibility, and introduces vulnerabilities.

## How to join The noJS Club

You can add your website to the list below as long as it uses no Javascript.

1. Make sure there is no Javascript on your website. Look for any `<script>` tags on your page.
2. Do a [GTMetrix scan](https://gtmetrix.com/) on your website.
3. If your site satisfies this requirement, [submit an issue](https://github.com/karan/nojs.club/issues/new?assignees=&labels=&template=nojsrequest.md&title=example.com) on GitHub.
4. Once the request is approved, the domain will be added to the list below.

## How it works

This repo uses Github Actions to automate adding a site to the data list.

* When issue opened (or edited or reopened), the action parses domain, gets `script` tags and comments with it.
* When I (`karan`) comment in a specific format (`/approve domain 123.45`), the action will add the site to the data and close the issue.

The website is served using Jekyll.

Based on the [1MB Club](https://1mb.club)
