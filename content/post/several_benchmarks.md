// * Summary *

BenchmarkDotNet=v0.10.10, OS=Windows 7 SP1 (6.1.7601.0)
Processor=Intel Xeon CPU X5670 2.93GHzIntel Xeon CPU X5670 2.93GHz, ProcessorCou
nt=24
Frequency=2863828 Hz, Resolution=349.1830 ns, Timer=TSC
  [Host]     : .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.6.
1099.0  [AttachedDebugger]
  DefaultJob : .NET Framework 4.6.1 (CLR 4.0.30319.42000), 32bit LegacyJIT-v4.6.
1099.0


                     Method |          Mean |     Error |    StdDev |
--------------------------- |--------------:|----------:|----------:|
           RunCompiledRegex |   787.3389 ns | 3.4260 ns | 3.2046 ns |
        RunNonCompiledRegex | 1,444.6535 ns | 2.3200 ns | 2.0566 ns |
  RunNonCompiledStaticRegex | 1,865.5567 ns | 1.4956 ns | 1.2489 ns |
        RunAssignmentWithOr |     0.0253 ns | 0.0080 ns | 0.0071 ns |
    RunAssignmentWithReturn |     0.0004 ns | 0.0008 ns | 0.0007 ns |
                    NewList |    52.4738 ns | 0.4124 ns | 0.3857 ns |
                   NewArray |    18.8899 ns | 0.0430 ns | 0.0359 ns |
              NewDictionary |    99.3509 ns | 0.6110 ns | 0.5715 ns |
            LoopUpdateArray |   136.3880 ns | 1.2316 ns | 1.1521 ns |
    LoopUpdateListUsingLinq |   176.7428 ns | 0.6221 ns | 0.5819 ns |
 LoopUpdateListUsingIndexer |   175.0030 ns | 1.4829 ns | 1.3871 ns |

// * Warnings *
Environment
  Summary -> Benchmark was executed with attached debugger

// * Hints *
Outliers
  RegexBenchmark.RunNonCompiledRegex: Default       -> 1 outlier  was  removed
  RegexBenchmark.RunNonCompiledStaticRegex: Default -> 2 outliers were removed
  RegexBenchmark.RunAssignmentWithOr: Default       -> 1 outlier  was  removed
  RegexBenchmark.RunAssignmentWithReturn: Default   -> 2 outliers were removed
  RegexBenchmark.NewArray: Default                  -> 2 outliers were removed

// * Legends *
  Mean   : Arithmetic mean of all measurements
  Error  : Half of 99.9% confidence interval
  StdDev : Standard deviation of all measurements
  1 ns   : 1 Nanosecond (0.000000001 sec)

// ***** BenchmarkRunner: End *****
// * Artifacts cleanup *
BenchmarkDotNet.Reports.Summary