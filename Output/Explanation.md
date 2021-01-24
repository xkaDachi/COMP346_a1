```
There are some of the reasons why we believe that there are different running times: 

-External programs or processes running outside this software (IDE) may have an impact on the individual thread running time each time we run our program. 

-There is no way to say which order the threads are being executed in, so in some of our executions there might be threads waiting for others. 
Whereas in subsequent running of this program, the command for thread execution can be modified to provide more effective running times.

-Hardware performance can also impact thread running time, if the program is running with different CPUs, the time for termination can vary from one another. 
Small timing discrepancies may be ok for our purposes, but a variety of other applications (such as trading) may need those millisecond gaps.
```
