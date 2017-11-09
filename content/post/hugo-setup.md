---
title: "Hugo Setup"
date: 2017-11-08
tags: ["Hugo"]
categories: ["static site generation"]
draft: false
---

## My Hugo Setup

Here's how I set up this site using the Hugo static site generator.

### Configuration for Hosting on Github
Since I host my site on Github, I followed the instructions on the Hugo site for [hosting on Github] (https://gohugo.io/hosting-and-deployment/hosting-on-github/)

I set my config.toml file to post to the "docs" dir in my github repo:
``` toml
baseurl = "http://www.onesolved.com"
publishDir = "docs"
title = "One Problem Solved"
```

### Default Post Template (Archtype)
When you add a post by running "hugo new post/new_post.md", it uses the template (json or toml format) in layouts/archtypes/default.md.
If you want to use the archtypes from a theme instead, then set the "theme" key in your config.toml file. Note that as long I as I have the "theme" key set, Hugo seems to prioritize the archtypes from the theme directory, as opposed to archtypes in my sites layouts/archtypes directory.

Documentation for archtypes is  on the [Hugo Site](https://gohugo.io/content-management/archetypes/)

Here is the content of my default.md archtype template:

```
title: "{{ replace .TranslationBaseName "_" " " | title }}"
date: {{ .Date }}
tags: []
categories: []
draft: true
```

