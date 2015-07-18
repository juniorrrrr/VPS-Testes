# Testing VPS performance using `unixbench`

Init:
```sh
wget http://byte-unixbench.googlecode.com/files/UnixBench5.1.3.tgz
tar zxf ./UnixBench5.1.3.tgz
cd ./UnixBench
./Run
```

### RunAbove Sandbox
- 1 core / 2 GB RAM / 20 GB SSD

```
Benchmark Run: Fri Jul 17 2015 16:05:25 - 16:33:31
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       28321147.1 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     4424.9 MWIPS (9.7 s, 7 samples)
Execl Throughput                               3278.8 lps   (29.8 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        656459.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          200313.3 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1611078.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1675927.1 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 173720.8 lps   (10.0 s, 7 samples)
Process Creation                               8076.9 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   4180.6 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                    550.1 lpm   (60.0 s, 2 samples)
System Call Overhead                        4007643.1 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   28321147.1   2426.8
Double-Precision Whetstone                       55.0       4424.9    804.5
Execl Throughput                                 43.0       3278.8    762.5
File Copy 1024 bufsize 2000 maxblocks          3960.0     656459.2   1657.7
File Copy 256 bufsize 500 maxblocks            1655.0     200313.3   1210.4
File Copy 4096 bufsize 8000 maxblocks          5800.0    1611078.2   2777.7
Pipe Throughput                               12440.0    1675927.1   1347.2
Pipe-based Context Switching                   4000.0     173720.8    434.3
Process Creation                                126.0       8076.9    641.0
Shell Scripts (1 concurrent)                     42.4       4180.6    986.0
Shell Scripts (8 concurrent)                      6.0        550.1    916.8
System Call Overhead                          15000.0    4007643.1   2671.8
                                                                   ========
System Benchmarks Index Score                                        1183.0
```

### EC2 Micro
- 1 core / 1 GB RAM / 8 GB

```
Benchmark Run: Fri Jul 17 2015 11:06:00 - 11:34:06
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       31026710.6 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     4072.5 MWIPS (9.8 s, 7 samples)
Execl Throughput                               3708.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        587829.9 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          154759.5 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1788349.4 KBps  (30.0 s, 2 samples)
Pipe Throughput                              785112.0 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 190703.6 lps   (10.0 s, 7 samples)
Process Creation                              12148.4 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   7130.1 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                    933.6 lpm   (60.0 s, 2 samples)
System Call Overhead                         539720.0 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   31026710.6   2658.7
Double-Precision Whetstone                       55.0       4072.5    740.4
Execl Throughput                                 43.0       3708.0    862.3
File Copy 1024 bufsize 2000 maxblocks          3960.0     587829.9   1484.4
File Copy 256 bufsize 500 maxblocks            1655.0     154759.5    935.1
File Copy 4096 bufsize 8000 maxblocks          5800.0    1788349.4   3083.4
Pipe Throughput                               12440.0     785112.0    631.1
Pipe-based Context Switching                   4000.0     190703.6    476.8
Process Creation                                126.0      12148.4    964.2
Shell Scripts (1 concurrent)                     42.4       7130.1   1681.6
Shell Scripts (8 concurrent)                      6.0        933.6   1556.0
System Call Overhead                          15000.0     539720.0    359.8
                                                                   ========
System Benchmarks Index Score                                        1058.8
```


### Digital Ocean
- 1 core / 512 MB RAM / 20 GB SSD

```
Benchmark Run: Fri Jul 17 2015 07:12:53 - 07:41:04
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       25960270.6 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     3393.9 MWIPS (9.9 s, 7 samples)
Execl Throughput                               2705.7 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        379994.0 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          102897.7 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1023008.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                              623227.2 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 149695.7 lps   (10.0 s, 7 samples)
Process Creation                               8203.4 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   5437.7 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                    701.6 lpm   (60.0 s, 2 samples)
System Call Overhead                         459888.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   25960270.6   2224.5
Double-Precision Whetstone                       55.0       3393.9    617.1
Execl Throughput                                 43.0       2705.7    629.2
File Copy 1024 bufsize 2000 maxblocks          3960.0     379994.0    959.6
File Copy 256 bufsize 500 maxblocks            1655.0     102897.7    621.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    1023008.3   1763.8
Pipe Throughput                               12440.0     623227.2    501.0
Pipe-based Context Switching                   4000.0     149695.7    374.2
Process Creation                                126.0       8203.4    651.1
Shell Scripts (1 concurrent)                     42.4       5437.7   1282.5
Shell Scripts (8 concurrent)                      6.0        701.6   1169.3
System Call Overhead                          15000.0     459888.8    306.6
                                                                   ========
System Benchmarks Index Score                                         780.4
```

### Digital Ocean
- 2 core / 2048 MB RAM / 40 GB SSD
```
Benchmark Run: Fri Jul 17 2015 11:38:18 - 12:06:34
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       22724725.9 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     2823.9 MWIPS (10.2 s, 7 samples)
Execl Throughput                               1821.8 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        686416.8 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          181075.4 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1342281.1 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1339067.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 201411.1 lps   (10.0 s, 7 samples)
Process Creation                               4513.1 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   5065.4 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1112.4 lpm   (60.0 s, 2 samples)
System Call Overhead                        2592839.3 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   22724725.9   1947.3
Double-Precision Whetstone                       55.0       2823.9    513.4
Execl Throughput                                 43.0       1821.8    423.7
File Copy 1024 bufsize 2000 maxblocks          3960.0     686416.8   1733.4
File Copy 256 bufsize 500 maxblocks            1655.0     181075.4   1094.1
File Copy 4096 bufsize 8000 maxblocks          5800.0    1342281.1   2314.3
Pipe Throughput                               12440.0    1339067.7   1076.4
Pipe-based Context Switching                   4000.0     201411.1    503.5
Process Creation                                126.0       4513.1    358.2
Shell Scripts (1 concurrent)                     42.4       5065.4   1194.7
Shell Scripts (8 concurrent)                      6.0       1112.4   1854.0
System Call Overhead                          15000.0    2592839.3   1728.6
                                                                   ========
System Benchmarks Index Score                                        1027.3

------------------------------------------------------------------------
Benchmark Run: Fri Jul 17 2015 12:06:34 - 12:34:48
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables       46740069.6 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     5854.9 MWIPS (9.4 s, 7 samples)
Execl Throughput                               5024.7 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        732393.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          211835.2 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1698947.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2604457.8 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 358606.8 lps   (10.0 s, 7 samples)
Process Creation                              10903.9 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   7118.1 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1278.3 lpm   (60.1 s, 2 samples)
System Call Overhead                        3184575.5 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   46740069.6   4005.1
Double-Precision Whetstone                       55.0       5854.9   1064.5
Execl Throughput                                 43.0       5024.7   1168.5
File Copy 1024 bufsize 2000 maxblocks          3960.0     732393.5   1849.5
File Copy 256 bufsize 500 maxblocks            1655.0     211835.2   1280.0
File Copy 4096 bufsize 8000 maxblocks          5800.0    1698947.2   2929.2
Pipe Throughput                               12440.0    2604457.8   2093.6
Pipe-based Context Switching                   4000.0     358606.8    896.5
Process Creation                                126.0      10903.9    865.4
Shell Scripts (1 concurrent)                     42.4       7118.1   1678.8
Shell Scripts (8 concurrent)                      6.0       1278.3   2130.5
System Call Overhead                          15000.0    3184575.5   2123.1
                                                                   ========
System Benchmarks Index Score                                        1656.3
```


### Vultr :clap: :metal:
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

### Scaleway
- 4 core (ARM) / 2048 MB RAM / 50 GB LSSD

```
Benchmark Run: Fri Jul 17 2015 15:22:39 - 15:50:56
0 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables        3659439.7 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                      557.7 MWIPS (9.9 s, 7 samples)
Execl Throughput                                939.9 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        104953.0 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks           29867.0 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks        292013.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                              195595.9 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  35128.8 lps   (10.0 s, 7 samples)
Process Creation                               2730.9 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   2010.2 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                    610.4 lpm   (60.1 s, 2 samples)
System Call Overhead                         653314.7 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0    3659439.7    313.6
Double-Precision Whetstone                       55.0        557.7    101.4
Execl Throughput                                 43.0        939.9    218.6
File Copy 1024 bufsize 2000 maxblocks          3960.0     104953.0    265.0
File Copy 256 bufsize 500 maxblocks            1655.0      29867.0    180.5
File Copy 4096 bufsize 8000 maxblocks          5800.0     292013.3    503.5
Pipe Throughput                               12440.0     195595.9    157.2
Pipe-based Context Switching                   4000.0      35128.8     87.8
Process Creation                                126.0       2730.9    216.7
Shell Scripts (1 concurrent)                     42.4       2010.2    474.1
Shell Scripts (8 concurrent)                      6.0        610.4   1017.3
System Call Overhead                          15000.0     653314.7    435.5
                                                                   ========
System Benchmarks Index Score                                         262.1
```