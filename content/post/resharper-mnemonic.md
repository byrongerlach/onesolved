title: "Resharper-Mnemonic"
date: 2018-01-09T10:37:46-08:00
tags: ["Resharper", "keyboard shortcuts"]
categories: ["commands and shortcuts"]
draft: true


## My Commonly-Used Shortcuts

Shortcut | Description
---------|------------
asdf | asdf


csharpTypes =
    "b", "bool"
    "c", "char"
    "f", "float"
    "by", "byte"
    "d", "double"
    "i", "int"
    "m", "decimal"
    "s", "string"
    "l", "long"
    "u", "uint"
    "g", "System.Guid"
    "t", "System.DateTime"
    "sb", "System.Text.StringBuilder"
  
cSharpStructureTemplates =
      "c", "public class "
      "a", "public abstract class "
      "C", "public static class "
      "i", "public interface "
      "s", "public struct "
      "e", "public enum"

cSharpMemberTemplates =
      "vr", "A readonly field of type "
      "V", "private static "
      "n", "A field of type FixedType initialized to the default value."
      "o", "A readonly field of type FixedType initialized to the default value."
      "t", Text "A test method. [Test] public void "
      "m", "A method that returns a FixedType "
      "M", "A static method that returns a FixedType"
      "p", "An automatic property of type FixedType
      "pr", "An automatic property of type FixedType  with a private setter"
      "pg", "An automatic property of type FixedType with an empty getter and no setter"

dotNetGenericTypes =
    "l.", "System.Collections.Generic.List"
    "h.",  "System.Collections.Generic.HashSet"
    *"di.", "System.Collections.Generic.Dictionary"
    "~",  "System.Collections.Generic.IEnumerable"