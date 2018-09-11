---
title: "TFS Commands"
date: 2018-09-04T12:00:46-08:00
tags: ["commands", "TFS", "source control"]
categories: ["commands and shortcuts"]
draft: false
---

## My Commonly-Used TFS Commands

### Folding in Vim

Shortcut | Description
---------|------------
tf history "$/<TFS project name>/<branch path>" /recursive /version:C<changeset>~T /format:detailed | 
Get detail of specific changeset
tf history "$/<TFS project name>/<branch path>" /recursive /stopafter:5 /noprompt  /format:detailed | Get detail of last 5 check-ins 
