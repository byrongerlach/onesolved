---
title : "Xunit for Dotnet Core"
description : ""
date : 2018-03-03
categories : ["testing"]
tags : ["testing", "xunit", "dotnet-core"]
draft : true
---

## XUnit

[XUnit Dotnet Core Documentation](https://xunit.github.io/docs/getting-started-dotnet-core)


## XUnit Assertions

XUnit's Assert automatically recognizes reference types and collections in C#. 

Therefore, two collections can be compared like this:

```
var actual = GetData();
var expected = new[] {"one", "two"};

Assert.Equal(expected, actual);
```