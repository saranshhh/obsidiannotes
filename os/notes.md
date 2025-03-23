process states:
1. new : secondary memory; sends to ready by Long Term Scheduler
2. ready: in RAM; queue: patch scheduler/short term scheduler to running
3. running: RAM; few processes can be sent back to ready due to priority / time quantum (in round robin schedulling) => premeptive; if theres no going back from running then non-preemptive (suspend ready if filled in RAM)
4. terminated: deallocation of memory
5. wait/block (from running -> goes to ready); when I/O is required for file or something in second memory (slow) so the process has to wait; so goes to ready (suspend wait if queue is filled in SM & goes to suspend ready)
![[Pasted image 20250213192601.png]]
Pre-emptive
1. SRTF; SHORTEST RUNNING FIRST 
2. LRTF
3. ROUND ROBIN
4. PRIORITY BASED

Non-pre-emptive:
1. FCFS: FIRST COME FIRST SERVE
2. SJF: SHORTEST JOB FIRST
3. LJF
4. HRRN: HIGHEST RESPONSE RATOI NEXT
5. Multilevel Queue

Arrival Time: time at which the process enters the queue
Burst Time: time reuqired by the process to executate on CPU (Duration)
Compute Time: at which the process completion (Point of time at completion)
Turn Around Time(TAT): CT-AT (Waiting Time: 12-11=1 => 60 mins)
Waiting Time: TWT - BT (60-20=>40 mins)
Response Time: time at which the process get first CPU execute - AT

1. FCFS (RT = WT)
criteria: Arrival Time & Non pre-emptive
1. SJF 
criteria: Burst Time & Non pre-emptive