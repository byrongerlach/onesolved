---
title: "Working Effectively With Legacy Code"
date: 2018-01-10T10:46:53-08:00
tags: ["unit testing", "refactoring"]
categories: ["books"]
draft: true
---

# Notes on Working Effectively With Legacy Code

*by Michael Feathers. Published by Prentice Hall, 2004* 

*Chapter 13: I need to Make a Change, but I Don't Know What Tests to Write*

> Automated tests are a very important tool, but not for bug finding—not directly, at least. In general,automated tests should specify a goal that we’d like to fulfill or attempt to preserve behavior that is already there. 

## Characterization Tests


Write a test to capture what the current code does. 

> Here is a little algorithm for writing characterization tests:
>
>1. Use a piece of code in a test harness.
>
>2. Write an assertion that you know will fail.
>
>3. Let the failure tell you what the behavior is.
>
>4. Change the test so that it expects the behavior that the >code produces.
>
>5. Repeat.


Questions that occur to me: 

1. Are there any existing tests for the current behavior? 
2. If not, can I write a characterization test for the current behavior? 
3. If the code is untestable without some huge effort, then is there a way to test a part of it? 