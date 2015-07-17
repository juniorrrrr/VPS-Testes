# Testing VPS performance using `unixbench`

### Vultr [vt]
- 2 core / 2048 MB RAM / 45 GB SSD

```
Benchmark Run: Fri Jul 17 2015 11:12:51 - 11:41:22
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       40825495.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     4124.6 MWIPS (12.7 s, 7 samples)
Execl Throughput                               4070.5 lps   (29.7 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1155143.3 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          339090.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2977468.0 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2739834.8 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  51034.5 lps   (10.0 s, 7 samples)
Process Creation                               9621.4 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   9245.4 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1723.0 lpm   (60.0 s, 2 samples)
System Call Overhead                        4896735.9 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   40825495.8   3498.3
Double-Precision Whetstone                       55.0       4124.6    749.9
Execl Throughput                                 43.0       4070.5    946.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    1155143.3   2917.0
File Copy 256 bufsize 500 maxblocks            1655.0     339090.9   2048.9
File Copy 4096 bufsize 8000 maxblocks          5800.0    2977468.0   5133.6
Pipe Throughput                               12440.0    2739834.8   2202.4
Pipe-based Context Switching                   4000.0      51034.5    127.6
Process Creation                                126.0       9621.4    763.6
Shell Scripts (1 concurrent)                     42.4       9245.4   2180.5
Shell Scripts (8 concurrent)                      6.0       1723.0   2871.7
System Call Overhead                          15000.0    4896735.9   3264.5
                                                                   ========
System Benchmarks Index Score                                        1623.1

------------------------------------------------------------------------
Benchmark Run: Fri Jul 17 2015 11:41:22 - 12:10:01
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables       76276527.3 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     7773.0 MWIPS (13.5 s, 7 samples)
Execl Throughput                               9646.2 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1401446.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          392756.1 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4229843.0 KBps  (30.0 s, 2 samples)
Pipe Throughput                             5058491.2 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 743451.0 lps   (10.0 s, 7 samples)
Process Creation                              17233.7 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  11273.3 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1949.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        7084549.4 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   76276527.3   6536.1
Double-Precision Whetstone                       55.0       7773.0   1413.3
Execl Throughput                                 43.0       9646.2   2243.3
File Copy 1024 bufsize 2000 maxblocks          3960.0    1401446.2   3539.0
File Copy 256 bufsize 500 maxblocks            1655.0     392756.1   2373.1
File Copy 4096 bufsize 8000 maxblocks          5800.0    4229843.0   7292.8
Pipe Throughput                               12440.0    5058491.2   4066.3
Pipe-based Context Switching                   4000.0     743451.0   1858.6
Process Creation                                126.0      17233.7   1367.8
Shell Scripts (1 concurrent)                     42.4      11273.3   2658.8
Shell Scripts (8 concurrent)                      6.0       1949.5   3249.1
System Call Overhead                          15000.0    7084549.4   4723.0
                                                                   ========
System Benchmarks Index Score                                        3001.8

```