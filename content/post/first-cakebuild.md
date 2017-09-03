---
title: "First Build Flow With Cakebuild"
description: "A description"
date: 2017-07-14T21:04:57-07:00
draft: true
tags: ["Cakebuild", "Dotnet", "Csharp"]
categories: ["Build Systems"]
series: ["Using Cakebuild"]

---

__Problem__: Development Builds Took Too Much Work to Configure

For a .NET application I work on, I wanted to have a more agile and faster development build and deployment process. Cakebuild had been on my radar, but seeing (person's) lighting talk at .NET Fringe 2017 on [Cakebuild](http://cakebuild.net) inspired me to give it a try.

## Cakebuild

[Cakebuild](http://cakebuild.net) is a cross-platform open source build system, driven by build scripts which use a C# domain-specific language.    

## Moving an Existing system to Cakebuild

[Cakebuild](http://cakebuild.net) uses a command-line "make-style" build process, where a C# script file defines the build process. My vision was to be able to invoke a [Cakebuild](http://cakebuild.net) script from the command line which would do combinations of the following tasks:

1. Checking out the source code from source control.
2. Updating configuration files in .NET projects
3. Building .NET solutions. 
4. Copying the built application to another location.

### Running Cakebuild

1. Download bootstrapper.
2. Run bootstrapper.

### Cakebuild Task Flow

1. Tasks
2. Dependencies

### Configuration with Cakebuild

My application uses XML configuration files, where XML attributes may contain server ports, addresses, database names, etc. Cakebuild makes updating XML files very easy using using [XmlPoke](http://cakebuild.net/api/Cake.Common.Xml/XmlPokeAliases/). 