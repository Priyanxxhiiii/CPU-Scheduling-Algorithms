# CPU-Scheduling-Algorithms
An implementation of various CPU scheduling algorithms. The algorithms included are First Come First Serve(FCFS), Shortest Job First(SJF), Shortest Remaining Time First(SRTF), Priority Scheduling(PS) and Round Robin(RR).
## Table of Contents
## Algorithms
### First Come First Serve (FCFS) (Non-preemptive)
- First Come First Serve (FCFS) is a CPU scheduling algorithm in which processes are executed on FCFS basis.
- The request or process which comes first in the ready queue is being executed first.
- This algorithm does not have any mechanism for prioritizing processes, so it is considered a **non-preemptive** algorithm.
- It is simple, easy-to-understand & easy-to-implement but poor in performance as average waiting time is high or we can say that it can lead to poor performance if there are processes with long burst times.

- In FCFS scheduling, the process that arrives first is executed first, regardless of its burst time or priority. This can lead to poor performance, as longer running processes will block shorter ones from being executed.
- It is commonly used in batch systems where the order of the processes is important.

### Shortest Job First(SJF) (Non-preemptive)
      Also know as:
      #### Shortest Job Next(SJN)
      #### Shortest Process Next(SPN)

- Drawback of First Come First Serve process is that, the job having highest burst time comes first then we have to execute it first even though in that time we can execute two or more process having shortest burst time.

- Shortest Job First(SJF) is a scheduling algorithm that prioritizes the execution of processes based on their burst time, or the amount of time they need to complete their task. It is a __non-preemptive algorithm__ which means that once a process starts executing, it runs until completion or until it enters a waiting state.

- The algorithm maintains a queue of processes, where each process is given a burst time when it arrives. __The process with the shortest burst time is executed first__, and as new processes arrive, they are added to the queue and sorted based on their burst time. The __process with the shortest burst time will always be at the front of the queue__, and thus will always be executed next.

- This algorithm can be beneficial in situations __where the objective is to minimize the average waiting time for processes__, since shorter processes will be executed first, and thus will spend less time waiting in the queue. However, it may cause starvation if shorter processes keep coming i.e., it can lead to longer running processes being blocked by shorter ones, which can negatively impact the overall performance of the system.

- In summary, SJF is a scheduling algorithm that prioritizes the execution of processes based on their burst time, it's non-preemptive and it's commonly used in situations where the objective is to minimize the average waiting time for processes.

### Shortest Remaining Time First - SJF in preemptive order
- Shortest remaining time first(SRTF) is the preemptive version of the SJF algorithm.

- The concept is same as Shortest Job First(SJF) that is we try to execute the job having smaller execution time first.

- The only difference is that in this algorithm we check at each interval the job queue and select the smallest process from it.

- The processor is allocated to the job closest to completion but it can be preempted by a 
newer ready job with shorter time to completion.
  
- Impossible to implement in interactive systems where required CPU time is not known.
  
- It is often used in batch environments where short jobs need to give preference.

### Priority Scheduling (Non-preemptive)
- Priority scheduling is a non-preemptive algorithm and one of the most common scheduling 
algorithms in batch systems.

- Each process is assigned a priority. Process with highest priority is to be executed first and 
so on.

- Processes with same priority are executed on first come first served basis.
  
- Priority can be decided based on memory requirements, time requirements or any other 
resource requirement.

### Round Robin with varying time quantum (RR) (Preemptive)
- The Round-robin scheduling algorithm is a kind of __preemptive First Come First Serve__ CPU Scheduling algorithm where each process in the ready state gets the CPU for a fixed time in a cyclic way (turn by turn).
  
- The RR scheduling algorithm is one of the CPU scheduling algorithms in which every process gets a fixed amount of time quantum to execute the process.
  
- In this algorithm, every process gets executed cyclically. This means that processes that have their burst time remaining after the expiration of the time quantum are sent back to the ready state and wait for their next turn to complete the execution until it terminates. This processing is done in FIFO order which suggests that processes are executed on a first-come, first-serve basis.

- The variable quantum allows the algorithm to be more efficient as it allows the CPU to spend more time on shorter processes and less time on longer ones. This can help to minimize the average waiting time for processes. Additionally, it also helps to avoid the issue of starvation, which occurs when a process with a long burst time prevents other processes from executing.

- #### How does the Round Robin Algorithm Work?
    1. All the processes are added to the ready queue.
       
    2. At first, the burst time of every process is compared to the time quantum of the CPU.
    
    3. If the burst time of the process is less than or equal to the time quantum in the round-robin scheduling algorithm, the process is executed to its burst time.
  
    4. If the burst time of the process is greater than the time quantum, the process is executed up to the time quantum (TQ).
  
    5. When the time quantum expires, it checks if the process is executed completely or not.
     
    6. On completion, the process terminates. Otherwise, it goes back again to the ready state.

 - Consider the below flow diagram for a better understanding of Round Robin scheduling algorithm:
![image](https://github.com/Priyanxxhiiii/CPU-Scheduling-Algorithms/assets/135419372/f148caf0-26e6-4eda-820d-3ca44d3b44df)











   

