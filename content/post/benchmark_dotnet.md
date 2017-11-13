---
title: "Benchmark DotNet"
date: 2017-11-12
tags: ["analytics"]
categories: []
draft: false
---

## Method-level Benchmarking Using BenchmarkDotNet

Here is an example of method-level benchmarking using BenchmarkDotNet. 

The [BenchmarkDotNet site](http://benchmarkdotnet.org/) provides [detailed instructions](http://benchmarkdotnet.org/Guides/GettingStarted.htm "BenchmarkDotNet's Website") for setup.

The following example shows a basic setup to benchmark two C# methods. 

### Creating a Console Application for Benchmarking

First, create a console application and install the BenchmarkDotNet Nuget package:

```
PM> Install-Package BenchmarkDotNet
```
The following example benchmarks two different methods of assigning new values based on comparisons:

``` csharp

using System;

using BenchmarkDotNet.Attributes;
using BenchmarkDotNet.Running;

namespace BenchmarkZoo
{

    public class MyBenchmark
    {
        private bool _b1, _b2;

        // Add the [Benchmark] attribute for methods you want to benchmark.
        [Benchmark]
        public void RunAssignmentWithOr()
        {
            _b1 = _b1 | _b2;
        }

        [Benchmark]
        public void RunAssignmentWithReturn()
        {
            if (_b1) return;

            _b1 = _b2;
        }
    }

    public class Program
    {
        public static void Main(string[] args)
        {
            var summary = BenchmarkRunner.Run<MyBenchmark>();

            Console.WriteLine(summary);
            Console.ReadKey();
        }
    }
}

```
<br>
### Running the Benchmark

Running the console program will run your annotated methods several times and generate a report including min, max, median, mean, and standard deviation for run times.

<pre>

// * Detailed results *
MyBenchmark.RunAssignmentWithOr: DefaultJob
Runtime = .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.7.2110.0; GC = Concurrent Workstation
Mean = 0.1586 ns, StdErr = 0.0044 ns (2.78%); N = 14, StdDev = 0.0165 ns
Min = 0.1401 ns, Q1 = 0.1464 ns, Median = 0.1533 ns, Q3 = 0.1755 ns, Max = 0.1908 ns
IQR = 0.0291 ns, LowerFence = 0.1027 ns, UpperFence = 0.2192 ns
ConfidenceInterval = [0.1400 ns; 0.1772 ns] (CI 99.9%), Margin = 0.0186 ns (11.71% of Mean)
Skewness = 0.75, Kurtosis = 1.94


MyBenchmark.RunAssignmentWithReturn: DefaultJob
Runtime = .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.7.2110.0; GC = Concurrent Workstation
Mean = 0.7755 ns, StdErr = 0.0203 ns (2.62%); N = 15, StdDev = 0.0785 ns
Min = 0.6153 ns, Q1 = 0.7390 ns, Median = 0.7826 ns, Q3 = 0.8309 ns, Max = 0.8943 ns
IQR = 0.0919 ns, LowerFence = 0.6011 ns, UpperFence = 0.9688 ns
ConfidenceInterval = [0.6915 ns; 0.8595 ns] (CI 99.9%), Margin = 0.0840 ns (10.83% of Mean)
Skewness = -0.42, Kurtosis = 2.45


Total time: 00:01:00 (60.91 sec)

// * Summary *

BenchmarkDotNet=v0.10.10, OS=Windows 10 Redstone 1 [1607, Anniversary Update] (10.0.14393.1770)
Processor=Intel Core i5-4210Y CPU 1.50GHz (Haswell), ProcessorCount=4
Frequency=1461458 Hz, Resolution=684.2482 ns, Timer=TSC
  [Host]     : .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.7.2110.0
  DefaultJob : .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.7.2110.0


                  Method |      Mean |     Error |    StdDev |
------------------------ |----------:|----------:|----------:|
     RunAssignmentWithOr | 0.1586 ns | 0.0186 ns | 0.0165 ns |
 RunAssignmentWithReturn | 0.7755 ns | 0.0840 ns | 0.0785 ns |

// * Hints *
Outliers
  MyBenchmark.RunAssignmentWithOr: Default -> 1 outlier  was  removed

// * Legends *
  Mean   : Arithmetic mean of all measurements
  Error  : Half of 99.9% confidence interval
  StdDev : Standard deviation of all measurements
  1 ns   : 1 Nanosecond (0.000000001 sec)

// ***** BenchmarkRunner: End *****
// * Artifacts cleanup *
BenchmarkDotNet.Reports.Summary

</pre>