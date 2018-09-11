---
title: "Hugo Setup"
date: 2017-11-08
tags: ["Hugo"]
categories: ["static site generation"]
draft: false
---

## My Hugo Setup
Here's how I set up this site using the [Hugo](https://gohugo.io/) static site generator.

### Themes 
There’s many available [themes](https://themes.gohugo.io/). I used the [Mainroad](https://themes.gohugo.io/mainroad/) theme, but I changed the colors. 

### Composing Posts 
To add a post, you just add a new [markdown](https://daringfireball.net/projects/markdown/syntax
) file with the correct metadata section at the top, and then run Hugo again to generate your static site. 

[Here’s an example](
https://raw.githubusercontent.com/byrongerlach/onesolved/master/content/post/vs-code-shortcuts.md) of what an actual posts look like written in markdown. This post is just making a table with a header above it, with a few tags, etc., in the metadata section at the top.

[This post](http://onesolved.com/post/prismjs/
) shows how I do the syntax highlighting on the site using PrismJS. 

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

### Configuration for Hosting on Github
Since I host my site on Github, I followed the instructions on the Hugo site for [hosting on Github] (https://gohugo.io/hosting-and-deployment/hosting-on-github/)

I set my config.toml file to post to the "docs" dir in my github repo:
``` toml
baseurl = "http://www.onesolved.com"
publishDir = "docs"
title = "One Problem Solved"
```

This is the [repository](https://github.com/byrongerlach/onesolved) for my site. 