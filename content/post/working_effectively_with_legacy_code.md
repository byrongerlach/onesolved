---
title: "Working Effectively With Legacy Code"
date: 2018-01-10T10:46:53-08:00
tags: ["unit testing", "refactoring"]
categories: ["books"]
draft: true
---

# Notes on Working Effectively With Legacy Code

*by Michael Feathers. Published by Prentice Hall, 2004* 


## Preface

### Attributes of Legacy Code

1. Somebody's else's code.
2. Code that you have to change, but you don't really understand.
3. Code without tests. [^1]


> With tests, we can change the behavior of our code quickly and verifiably. Without them, we really don’t know if our code is getting better or worse. [^1]

[^1]: Preface, **Working Effectively With Legacy Code**.

## Chapter 1: Changing Software

Four Reasons to Change Software

1. Adding a feature

2. Fixing a bug

3. Improving the design

4. Optimizing resource usage [^2]

[^2]: Chapter 1: Changing Software, **Working Effectively With Legacy Code**.

### Chapter 2: Working with Feedback

The Legacy Code Change Algorithm

When you have to make a change in a legacy code base, here is an algorithm you can use.

1. Identify change points.

2. Find test points.

3. Break dependencies.

4. Write tests.

5. Make changes and refactor. [^2]

[^3]: Chapter 2: Working with Feedback, **Working Effectively With Legacy Code**.

## Chapter 6: I Don't Have Much Time and I Have to Change It

### Sprout Method

>When you need to add a feature to a system and it can be formulated completely as new code, write the code in a new method. 
[^3]: Chapter 6: I Don't Have Much Time and I Have to Change It, **Working Effectively With Legacy Code**.


### Sprout Class

When refactoring a method or class seems infeasible, create a new class to hold your changes and use it from the source class[^4].
[^3]: Chapter 6: I Don't Have Much Time and I Have to Change It, **Working Effectively With Legacy Code**.


## Chapter 10: 

### Chapter 25 Dependency-Breaking Techniques

#### Extract Interface

In order to break a dependency to a concrete implementation, create an interface for the dependency and use it in the test. 
[Extract Interface](https://www.safaribooksonline.com/library/view/working-effectively-with/0131177052/ch25.html#ch25sec1lev10)

## Questions: 

1. Are there any existing tests for the current behavior? 
2. If not, can I write a characterization test for the current behavior? 
3. If the code is untestable without some huge effort, then is there a way to test a part of it? 


## Appendix: Refactoring

### Extract Method

If you need to change behavior inside of a method, consider encapsulating that behavior in a new method.

## Chapter 13: I need to Make a Change, but I Don't Know What Tests to Write ##

> Automated tests are a very important tool, but not for bug finding—not directly, at least. In general,automated tests should specify a goal that we’d like to fulfill or attempt to preserve behavior that is already there. 


## Chapter 13: I need to Make a Change, but I Don't Know What Tests to Write ##

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
>4. Change the test so that it expects the behavior that the code produces.
>
>5. Repeat. [^5]

