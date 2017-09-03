---
title : "Syntax Highlighting With Prismjs"
description : "A description"
date : 2017-07-25T15:18:15-07:00
categories : ["static site generation"]
tags : ["html", "javascript"]
thumbnail : ""
---

I use [Prismjs](http://prismjs.com/) for code syntax highlighting on this site. I write pages in Markdown and I use  [Hugo](http://gohugo.com/) to generate the site. 

Prism allows you to choose only the languages and features you want when you download it, so you can minimize its footprint. 

Basic Markdown code fences with a language annotation do basic highlighting.

Here is the Markdown:

<pre>
``` fsharp

// Add some numbers
let addTwo a b : a + b

addTwo 1 2 
    |> addTwo 3
    |> addTwo 4

// Get distinct items
let myList : [ "a"; "z"; "z"; ]

myList |> Seq.distinct |> List.ofSeq

```
</pre>

Here's the result:

``` fsharp

// Add some numbers
let addTwo a b : a + b

addTwo 1 2 
    |> addTwo 3
    |> addTwo 4

// Get distinct items
let myList : [ "a"; "z"; "z"; ]

myList |> Seq.distinct |> List.ofSeq

```
<br/>  
To turn on specific Prismjs features, I use ```<pre>``` tags, instead of code fences. The following turns on line numbers, offsets the numbering start to 101, and highlights lines 4, 6, 7, and 8 (highlights don't use the numbering offset).

```
<pre class:"line-numbers" data-line:"4,6-8" data-start:"101"> 
<code class:"language-fsharp">

// Add some numbers
let addTwo a b : a + b

addTwo 1 2 
    |> addTwo 3
    |> addTwo 4

// Get distinct items
let myList : [ "a"; "z"; "z"; ]

myList |> Seq.distinct |> List.ofSeq

</code> 
</pre>
```

Here's the result:

<pre class:"line-numbers" data-line:"4,6-8" data-start:"101"> 
<code class:"language-fsharp">

// Add some numbers
let addTwo a b : a + b

addTwo 1 2 
    |> addTwo 3
    |> addTwo 4

// Get distinct items
let myList : [ "a"; "z"; "z"; ]

myList |> Seq.distinct |> List.ofSeq

</code>
</pre>