###### Additional task to complete performance course

The goal was to create a simple spring application and measure performance using different tools:

* top (screenshot #1). Looking for a pid of process first 
```
ps aux | grep -i "payrollApplication"
```
 then use 
 ```
 top -pid 95773
```
* uptime (screenshot #2). To check only load average of CPU before and after launching the application. 

* 




The example application was taken from [here](https://spring.io/guides/tutorials/bookmarks/).