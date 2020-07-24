###### Additional task to complete performance course

The goal was to create a simple spring application and measure performance using different tools and system utils.

General utils to gather some data: 

* top (screenshot #1). Looking for a pid of process first: 
```
ps aux | grep -i "payrollApplication"
```
 then use:
 ```
 top -pid 95773
```
* uptime (screenshot #2). To check only load average of CPU before and after launching the application. 

The following commands could be used to identify potential bottlenecks in i/o devices loading, cpu and memory usage, according to [this](http://www.brendangregg.com/USEmethod/use-linux.html) checklist.

* vmstat (screenshot #3).

* iostat (screenshot #4).

* Alternative to command free - to know how much memory is available (screenshot #11):
```
sysctl -a | awk '/hw./' && '/mem/'
```
Java monitoring utilities:

* jcmd (screenshot #5, #6).
 ```
 jcmd <PID> PerfCounter.print
```
 ```
 jcmd <PID> Thread.print
```
* VisualVM (screenshot #7, #8, #9).

* Heap Dump Analysis with IBMHelpAnalyzer to identify potential java heap leaks (screenshot #10). 




The example application was taken from [here](https://spring.io/guides/tutorials/bookmarks/).