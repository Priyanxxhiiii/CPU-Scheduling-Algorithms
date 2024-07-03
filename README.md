# CPU-Scheduling-Algorithms
An implementation of various CPU scheduling algorithms. The algorithms included are First Come First Serve(FCFS), Round Robin(RR), Shortest Job First(SJF), Priority Scheduling(PS), and Shortest Remaining Time First(SRTF).
## Table of Contents
## Algorithms
### First Come First Serve(FCFS)
- First Come First Serve (FCFS) is a CPU scheduling algorithm in which processes are executed on FCFS basis.
- The request or process which comes first in the ready queue is being executed first.
- - This algorithm does not have any mechanism for prioritizing processes, so it is considered a non-preemptive algorithm.
- It is simple, easy-to-understand & easy-to-implement but poor in performance as average waiting time is high or we can say that it can lead to poor performance if there are processes with long burst times.

- In FCFS scheduling, the process that arrives first is executed first, regardless of its burst time or priority. This can lead to poor performance, as longer running processes will block shorter ones from being executed.
- It is commonly used in batch systems where the order of the processes is important.
