# Comparing Things in C#

## Comparing Reference Types

Common ways to compare reference types in C# are: 

1. The "==" operator
2. .Equals
3. Comparator

### The == operator

MSDN: 
https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/equality-comparison-operator

"For predefined value types, the equality operator (==) returns true if the values of its operands are equal, false otherwise. For reference types other than string, == returns true if its two operands refer to the same object. For the string type, == compares the values of the strings."

Above, what does "same object" mean? An object occupying the same memory address? 

.. constant versus instance, read this: 

https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/equality-comparison-operator


Equals requires an object to exist
https://stackoverflow.com/a/144562

http://thedailywtf.com/articles/SkillsEquals(null)



The == operator returns true if two objects are the same object. 

### Value Types 

in C# 

Below is the resulting IL code for: 

```int a = 1;

if (a == 1) {}
```


IL_0000:  nop         
IL_0001:  ldc.i4.1    
IL_0002:  stloc.0     // a
IL_0003:  ldloc.0     // a
IL_0004:  ldc.i4.1    
IL_0005:  ceq         
IL_0007:  stloc.1     
IL_0008:  ldloc.1     
IL_0009:  brfalse.s   IL_000D
IL_000B:  nop         
IL_000C:  nop         
IL_000D:  ret  


Below is the resulting IL code from using .Equals on a value type.

the main reason I know of overriding .Equals for a value type is described here: 

https://msdn.microsoft.com/en-us/library/2dts52z7(v=vs.110).aspx

quote:
Particularly if your value type contains fields that are reference types, you should override the Equals(Object) method. This can improve performance and enable you to more closely represent the meaning of equality for the type.


```int a = 1;
if (a.Equals(1)) { }
```


IL_0000:  nop         
IL_0001:  ldc.i4.1    
IL_0002:  stloc.0     // a
IL_0003:  ldloca.s    00 // a
IL_0005:  ldc.i4.1    
IL_0006:  call        System.Int32.Equals
IL_000B:  stloc.1     
IL_000C:  ldloc.1     
IL_000D:  brfalse.s   IL_0011
IL_000F:  nop         
IL_0010:  nop         
IL_0011:  ret 