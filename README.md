# CPU-Scheduling-Algorithms
An implementation of various CPU scheduling algorithms. The algorithms included are First Come First Serve(FCFS), Round Robin(RR), Shortest Job First(SJF), Priority Scheduling(PS), and Shortest Remaining Time First(SRTF).
## Table of Contents
## Algorithms
### First Come First Serve (FCFS)
- First Come First Serve (FCFS) is a CPU scheduling algorithm in which processes are executed on FCFS basis.
- The request or process which comes first in the ready queue is being executed first.
- This algorithm does not have any mechanism for prioritizing processes, so it is considered a **non-preemptive** algorithm.
- It is simple, easy-to-understand & easy-to-implement but poor in performance as average waiting time is high or we can say that it can lead to poor performance if there are processes with long burst times.

- In FCFS scheduling, the process that arrives first is executed first, regardless of its burst time or priority. This can lead to poor performance, as longer running processes will block shorter ones from being executed.
- It is commonly used in batch systems where the order of the processes is important.

### Round Robin with varying time quantum (RR)
- The Round-robin scheduling algorithm is a kind of __preemptive First Come First Serve__ CPU Scheduling algorithm where each process in the ready state gets the CPU for a fixed time in a cyclic way (turn by turn).
  
- The RR scheduling algorithm is one of the CPU scheduling algorithms in which every process gets a fixed amount of time quantum to execute the process.
  
- In this algorithm, every process gets executed cyclically. This means that processes that have their burst time remaining after the expiration of the time quantum are sent back to the ready state and wait for their next turn to complete the execution until it terminates. This processing is done in FIFO order which suggests that processes are executed on a first-come, first-serve basis.
