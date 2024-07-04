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

#### How does the Round Robin Algorithm Work?
1. All the processes are added to the ready queue.
2. At first, The burst time of every process is compared to the time quantum of the CPU.
3. If the burst time of the process is less than or equal to the time quantum in the round-robin scheduling algorithm, the process is executed to its burst time.
4. If the burst time of the process is greater than the time quantum, the process is executed up to the time quantum (TQ).
5. When the time quantum expires, it checks if the process is executed completely or not.
6. On completion, the process terminates. Otherwise, it goes back again to the ready state.
