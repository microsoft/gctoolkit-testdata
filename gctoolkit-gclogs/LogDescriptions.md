# cfm.concurrent-mark.log


* A log of coldfusion?
* ParNew
* Concurrent mark and sweep 

#### Current Errors From Censum


listed as issue #4 :

```
29-May-2012 16:47:58 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 95.739: [GC [1 CMS-initial-mark: 230544K(524288K)] 488950K(873856K), 0.2253252 secs] [Times: user=0.22 sys=0.00, real=0.22 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 16:47:58 com.kodewerk.censum.parser.CMSTenuredPoolParser processCMSRevertToFull
SEVERE: concurrent mode failure 99.269: [Full GC 99.270: [CMS99.325: [CMS-concurrent-mark: 1.598/3.360 secs] [Times: user=9.57 sys=0.44, real=3.36 secs]
29-May-2012 16:47:58 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 101.125: [GC [1 CMS-initial-mark: 172938K(524288K)] 307917K(873856K), 0.0737873 secs] [Times: user=0.08 sys=0.00, real=0.08 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 16:47:58 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 101.662: [CMS-concurrent-mark: 0.312/0.463 secs] [Times: user=1.36 sys=0.06, real=0.46 secs]
29-May-2012 16:47:58 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose Full GC (concurrent mode failure)@93.087
29-May-2012 16:47:58 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose Full GC (concurrent mode failure)@99.269
```

# gc_20080331113608.log

* ParNew
* Concurrent mark and sweep 

#### Current Errors From Censum

UI was DOA, no output shown.

```
29-May-2012 17:32:38 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@5273.802
29-May-2012 17:32:42 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@10180.87
29-May-2012 17:32:43 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 20755.204: [GC [1 CMS-initial-mark: 968495K(2015232K)] 968499K(2097088K), 0.0386990 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:32:43 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 20762.304: [CMS-concurrent-mark: 5.404/7.061 secs]
29-May-2012 17:32:43 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 20764.231: [CMS-concurrent-preclean: 1.465/1.927 secs]
29-May-2012 17:32:43 com.kodewerk.censum.parser.CMSTenuredPoolParser processRemark
SEVERE: remark choked on 20764.349: [GC[YG occupancy: 81581 K (81856 K)]20764.350: [Rescan (parallel) , 0.0586887 secs]20764.409: [weak refs processing, 0.0015838 secs] [1 CMS-remark: 1034137K(2015232K)] 1115719K(2097088K), 0.0610514 secs]
Exception in thread "GCLogParser:JavaHeap" java.lang.NullPointerException
	at com.kodewerk.censum.parser.JavaHeapParser.icmsParNewOrDerNewDetialsWithTenuring(JavaHeapParser.java:189)
	at com.kodewerk.censum.parser.JavaHeapParser.process(JavaHeapParser.java:99)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
```

# gc_201103111820_JAVA_OPTS37_crash.log

* ParNew
* Concurrent mark and sweep 

#### Current Errors From Censum


```
29-May-2012 17:46:20 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 4269.891: [GC [1 CMS-initial-mark: 11729402K(14680064K)] 11760282K(16567552K), 0.0141450 secs] [Times: user=0.01 sys=0.00, real=0.02 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:20 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 4295.771: [CMS-concurrent-mark: 6.848/25.856 secs] (CMS-concurrent-mark yielded 201 times)
29-May-2012 17:46:21 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 4879.853: [GC [1 CMS-initial-mark: 8711719K(14680064K)] 8923502K(16567552K), 0.1596490 secs] [Times: user=0.16 sys=0.00, real=0.16 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:21 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 4905.000: [CMS-concurrent-mark: 9.495/24.988 secs] (CMS-concurrent-mark yielded 205 times)
29-May-2012 17:46:21 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 4937.695: [GC [1 CMS-initial-mark: 8841704K(14680064K)] 9065905K(16567552K), 0.2046950 secs] [Times: user=0.21 sys=0.00, real=0.21 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:21 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 4947.483: [CMS-concurrent-mark: 6.257/9.583 secs] (CMS-concurrent-mark yielded 63 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26165.616: [GC [1 CMS-initial-mark: 8697605K(14680064K)] 8809106K(16567552K), 0.1340060 secs] [Times: user=0.13 sys=0.00, real=0.14 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26194.236: [CMS-concurrent-mark: 9.135/28.487 secs] (CMS-concurrent-mark yielded 208 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26232.788: [GC [1 CMS-initial-mark: 8849307K(14680064K)] 9059146K(16567552K), 0.1351250 secs] [Times: user=0.13 sys=0.00, real=0.14 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26283.940: [CMS-concurrent-mark: 14.567/51.016 secs] (CMS-concurrent-mark yielded 108 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26310.472: [GC [1 CMS-initial-mark: 8707159K(14680064K)] 8773274K(16567552K), 0.0737630 secs] [Times: user=0.07 sys=0.00, real=0.07 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26344.952: [CMS-concurrent-mark: 15.920/34.406 secs] (CMS-concurrent-mark yielded 120 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26374.800: [GC [1 CMS-initial-mark: 8753334K(14680064K)] 8963995K(16567552K), 0.1735960 secs] [Times: user=0.17 sys=0.00, real=0.18 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26426.307: [CMS-concurrent-mark: 14.914/51.332 secs] (CMS-concurrent-mark yielded 100 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26451.526: [GC [1 CMS-initial-mark: 8320786K(14680064K)] 8348213K(16567552K), 0.0372840 secs] [Times: user=0.04 sys=0.00, real=0.04 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26516.996: [CMS-concurrent-mark: 20.699/65.433 secs] (CMS-concurrent-mark yielded 148 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26547.705: [GC [1 CMS-initial-mark: 10684348K(14680064K)] 10700386K(16567552K), 0.0253510 secs] [Times: user=0.03 sys=0.00, real=0.02 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26577.546: [CMS-concurrent-mark: 13.583/29.815 secs] (CMS-concurrent-mark yielded 110 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26616.469: [GC [1 CMS-initial-mark: 8599481K(14680064K)] 8813222K(16567552K), 0.0997840 secs] [Times: user=0.10 sys=0.00, real=0.10 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26658.277: [CMS-concurrent-mark: 18.209/41.708 secs] (CMS-concurrent-mark yielded 79 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26686.837: [GC [1 CMS-initial-mark: 10110861K(14680064K)] 10130061K(16567552K), 0.0172390 secs] [Times: user=0.02 sys=0.00, real=0.01 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26726.463: [CMS-concurrent-mark: 8.026/39.609 secs] (CMS-concurrent-mark yielded 126 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26743.053: [GC [1 CMS-initial-mark: 4451459K(14680064K)] 4750015K(16567552K), 0.2266760 secs] [Times: user=0.23 sys=0.00, real=0.23 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26825.821: [CMS-concurrent-mark: 22.887/82.541 secs] (CMS-concurrent-mark yielded 193 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26858.143: [GC [1 CMS-initial-mark: 11646070K(14680064K)] 11669003K(16567552K), 0.0257260 secs] [Times: user=0.02 sys=0.00, real=0.03 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26916.738: [CMS-concurrent-mark: 8.161/58.564 secs] (CMS-concurrent-mark yielded 98 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 26942.437: [GC [1 CMS-initial-mark: 6454720K(14680064K)] 6666659K(16567552K), 0.1535390 secs] [Times: user=0.15 sys=0.00, real=0.16 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 26981.923: [CMS-concurrent-mark: 14.387/39.333 secs] (CMS-concurrent-mark yielded 171 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27012.592: [GC [1 CMS-initial-mark: 10782498K(14680064K)] 10810669K(16567552K), 0.0419240 secs] [Times: user=0.04 sys=0.00, real=0.04 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27063.916: [CMS-concurrent-mark: 18.631/51.282 secs] (CMS-concurrent-mark yielded 115 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27096.313: [GC [1 CMS-initial-mark: 11265133K(14680064K)] 11657710K(16567552K), 0.3369890 secs] [Times: user=0.34 sys=0.00, real=0.34 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27156.753: [CMS-concurrent-mark: 12.582/60.102 secs] (CMS-concurrent-mark yielded 82 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27188.131: [GC [1 CMS-initial-mark: 8840754K(14680064K)] 9056137K(16567552K), 0.2382610 secs] [Times: user=0.24 sys=0.00, real=0.24 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27240.550: [CMS-concurrent-mark: 18.425/52.180 secs] (CMS-concurrent-mark yielded 136 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27268.474: [GC [1 CMS-initial-mark: 9715936K(14680064K)] 9766236K(16567552K), 0.0616940 secs] [Times: user=0.06 sys=0.00, real=0.06 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27297.062: [CMS-concurrent-mark: 9.996/28.526 secs] (CMS-concurrent-mark yielded 157 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27333.629: [GC [1 CMS-initial-mark: 8784089K(14680064K)] 9010779K(16567552K), 0.1739820 secs] [Times: user=0.18 sys=0.00, real=0.17 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27366.861: [CMS-concurrent-mark: 8.197/33.057 secs] (CMS-concurrent-mark yielded 80 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27412.776: [GC [1 CMS-initial-mark: 8947159K(14680064K)] 9184283K(16567552K), 0.1396600 secs] [Times: user=0.14 sys=0.00, real=0.14 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27435.797: [CMS-concurrent-mark: 8.677/22.881 secs] (CMS-concurrent-mark yielded 35 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27479.631: [GC [1 CMS-initial-mark: 8902915K(14680064K)] 9112696K(16567552K), 0.1623440 secs] [Times: user=0.16 sys=0.00, real=0.16 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27498.105: [CMS-concurrent-mark: 8.829/18.312 secs] (CMS-concurrent-mark yielded 16 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27539.349: [GC [1 CMS-initial-mark: 8793848K(14680064K)] 9054750K(16567552K), 0.1340400 secs] [Times: user=0.13 sys=0.00, real=0.13 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27572.717: [CMS-concurrent-mark: 10.770/33.229 secs] (CMS-concurrent-mark yielded 51 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27602.893: [GC [1 CMS-initial-mark: 8601624K(14680064K)] 8826532K(16567552K), 0.1596570 secs] [Times: user=0.16 sys=0.00, real=0.16 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27621.347: [CMS-concurrent-mark: 9.102/18.294 secs] (CMS-concurrent-mark yielded 42 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27658.346: [GC [1 CMS-initial-mark: 8654037K(14680064K)] 9145829K(16567552K), 0.4143000 secs] [Times: user=0.40 sys=0.00, real=0.42 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27703.032: [CMS-concurrent-mark: 12.251/44.272 secs] (CMS-concurrent-mark yielded 27 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27727.801: [GC [1 CMS-initial-mark: 6943780K(14680064K)] 7434610K(16567552K), 0.2150800 secs] [Times: user=0.22 sys=0.00, real=0.21 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27765.504: [CMS-concurrent-mark: 10.179/37.488 secs] (CMS-concurrent-mark yielded 130 times)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27807.623: [GC [1 CMS-initial-mark: 8673287K(14680064K)] 8883573K(16567552K), 0.1811180 secs] [Times: user=0.18 sys=0.00, real=0.18 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
29-May-2012 17:46:23 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27843.526: [CMS-concurrent-mark: 15.211/35.721 secs] (CMS-concurrent-mark yielded 46 times)
Exception in thread "GCLogParser:JavaHeap" java.lang.NullPointerException
	at com.kodewerk.censum.parser.JavaHeapParser.parNewOrDefNewDetailsWithTenuring(JavaHeapParser.java:167)
	at com.kodewerk.censum.parser.JavaHeapParser.process(JavaHeapParser.java:75)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
```


# lmax3.log

* ParNew
* Concurrent mark and sweep 

#### Current Errors From Censum

* UI functions despite errors

```
30-May-2012 10:15:19 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 3.787: [GC [1 CMS-initial-mark: 24447K(2960704K)] 92610K(3127232K), 0.0373950 secs] [Times: user=0.04 sys=0.00, real=0.04 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
```



# par.cms.wd.wt.log

* ParNew
* Concurrent mark and sweep 

#### Current Errors From Censum

* UI functions despite errors

```
30-May-2012 10:17:45 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@15.598
30-May-2012 10:17:45 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 18.309: [GC [1 CMS-initial-mark: 55146K(64768K)] 55835K(83392K), 0.0006993 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 18.404: [CMS-concurrent-mark: 0.078/0.094 secs] [Times: user=0.15 sys=0.01, real=0.10 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 18.405: [CMS-concurrent-preclean: 0.001/0.001 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 23.570: [GC [1 CMS-initial-mark: 58405K(64768K)] 62606K(83392K), 0.0008419 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 23.652: [CMS-concurrent-mark: 0.068/0.081 secs] [Times: user=0.12 sys=0.01, real=0.09 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 23.652: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose Full GC (concurrent mode failure)@18.828
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27.008: [GC [1 CMS-initial-mark: 46421K(64768K)] 46791K(83392K), 0.0009154 secs] [Times: user=0.01 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27.096: [CMS-concurrent-mark: 0.075/0.087 secs] [Times: user=0.13 sys=0.00, real=0.09 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 27.096: [CMS-concurrent-preclean: 0.001/0.001 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processRemark
SEVERE: remark choked on 28.149: [GC[YG occupancy: 2460 K (18624 K)]28.149: [Rescan (parallel) , 0.0013716 secs]28.150: [weak refs processing, 0.0000055 secs] [1 CMS-remark: 63744K(64768K)] 66204K(83392K), 0.0014571 secs] [Times: user=0.01 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@24.034
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 37.001: [GC [1 CMS-initial-mark: 47977K(64768K)] 49080K(83392K), 0.0007649 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 37.073: [CMS-concurrent-mark: 0.068/0.071 secs] [Times: user=0.07 sys=0.00, real=0.08 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 37.073: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 44.076: [GC [1 CMS-initial-mark: 45149K(64768K)] 60446K(83392K), 0.0009316 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 44.167: [CMS-concurrent-mark: 0.072/0.090 secs] [Times: user=0.14 sys=0.00, real=0.09 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 44.168: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@34.611
30-May-2012 10:17:48 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@41.597
```


# PoseidonDevGC.log

N.B I am not sure on these ones...need to understand this log better

* Default New
* Concurrent mark and sweep 


#### Current Errors From Censum

* UI functions despite errors

```
30-May-2012 10:17:45 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@15.598
30-May-2012 10:17:45 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 18.309: [GC [1 CMS-initial-mark: 55146K(64768K)] 55835K(83392K), 0.0006993 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 18.404: [CMS-concurrent-mark: 0.078/0.094 secs] [Times: user=0.15 sys=0.01, real=0.10 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 18.405: [CMS-concurrent-preclean: 0.001/0.001 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 23.570: [GC [1 CMS-initial-mark: 58405K(64768K)] 62606K(83392K), 0.0008419 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 23.652: [CMS-concurrent-mark: 0.068/0.081 secs] [Times: user=0.12 sys=0.01, real=0.09 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 23.652: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose Full GC (concurrent mode failure)@18.828
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 27.008: [GC [1 CMS-initial-mark: 46421K(64768K)] 46791K(83392K), 0.0009154 secs] [Times: user=0.01 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 27.096: [CMS-concurrent-mark: 0.075/0.087 secs] [Times: user=0.13 sys=0.00, real=0.09 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 27.096: [CMS-concurrent-preclean: 0.001/0.001 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.CMSTenuredPoolParser processRemark
SEVERE: remark choked on 28.149: [GC[YG occupancy: 2460 K (18624 K)]28.149: [Rescan (parallel) , 0.0013716 secs]28.150: [weak refs processing, 0.0000055 secs] [1 CMS-remark: 63744K(64768K)] 66204K(83392K), 0.0014571 secs] [Times: user=0.01 sys=0.00, real=0.00 secs]
30-May-2012 10:17:46 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@24.034
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 37.001: [GC [1 CMS-initial-mark: 47977K(64768K)] 49080K(83392K), 0.0007649 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 37.073: [CMS-concurrent-mark: 0.068/0.071 secs] [Times: user=0.07 sys=0.00, real=0.08 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 37.073: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processInitialMark
SEVERE: initial-mark choked on 44.076: [GC [1 CMS-initial-mark: 45149K(64768K)] 60446K(83392K), 0.0009316 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
java.lang.IllegalStateException: previous CMS collection event was not recorded
	at com.kodewerk.censum.memory.CMSTenuredPool.initialMark(CMSTenuredPool.java:22)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.processInitialMark(CMSTenuredPoolParser.java:87)
	at com.kodewerk.censum.parser.CMSTenuredPoolParser.process(CMSTenuredPoolParser.java:37)
	at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
	at java.lang.Thread.run(Thread.java:662)
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentMarkEnd
SEVERE: concurrent-mark choked on 44.167: [CMS-concurrent-mark: 0.072/0.090 secs] [Times: user=0.14 sys=0.00, real=0.09 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.CMSTenuredPoolParser processConcurrentPrecleanEnd
SEVERE: pre-clean choked on 44.168: [CMS-concurrent-preclean: 0.000/0.000 secs] [Times: user=0.00 sys=0.00, real=0.00 secs]
30-May-2012 10:17:47 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@34.611
30-May-2012 10:17:48 com.kodewerk.censum.parser.JavaHeapParser initMemoryPoolState
SEVERE: About to lose ParNew (promotion failed)@41.597
```

# SerialGC.log

* Serial gc

N.B I am not sure on these ones

#### No Errors From Censum




#par.icms.wd.nt.ast.2.log

fine


#par.icms.wd.nt.ast.log

fine



# par.oldpar.wd.nt.ast.log

```
java.lang.ArrayIndexOutOfBoundsException: 1                                                                                                                                                     
        at com.kodewerk.censum.util.StringUtils.parseFromToCapacity(StringUtils.java:75)                                                                                                        
        at com.kodewerk.censum.parser.YoungGenerationParser.process(YoungGenerationParser.java:51)                                                                                              
        at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)                                                                                                                      
        at java.lang.Thread.run(Thread.java:662)
```


# par.par.wd.nt.log

```
[WARNING] 
java.lang.ArrayIndexOutOfBoundsException: 1
        at com.kodewerk.censum.util.StringUtils.parseFromToCapacity(StringUtils.java:75)
        at com.kodewerk.censum.parser.YoungGenerationParser.process(YoungGenerationParser.java:51)
        at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
        at java.lang.Thread.run(Thread.java:662)
[WARNING] 
java.lang.NullPointerException
        at com.kodewerk.censum.parser.JavaHeapParser.fillOutMemoryPoolState(JavaHeapParser.java:132)
        at com.kodewerk.censum.parser.JavaHeapParser.youngGenWithTenuringDetails(JavaHeapParser.java:336)
        at com.kodewerk.censum.parser.JavaHeapParser.process(JavaHeapParser.java:119)
        at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
        at java.lang.Thread.run(Thread.java:662)
```




# psyg.cms.wd.nt.log

```
java.lang.ArrayIndexOutOfBoundsException: 1
        at com.kodewerk.censum.util.StringUtils.parseFromToCapacity(StringUtils.java:75)
        at com.kodewerk.censum.parser.YoungGenerationParser.process(YoungGenerationParser.java:51)
        at com.kodewerk.censum.parser.GCLogParser.run(GCLogParser.java:36)
        at java.lang.Thread.run(Thread.java:662)
```