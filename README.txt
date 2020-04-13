OS Scheduling Simulator.

Made by Nicholas Pumper and Yuki Suzuki. 
Do NOT copy or claim as your own.
Made for a class taught by Thomas Mirrinan.

to run: ./bin/osscheduler ./resrc/configfilehere.txtexample command you can run out of the box: ./bin/osscheduler ./resrc/config_01.txt


Use txt files as config files to customize how it simulates processes.
Example config files are in the resrc folder.
Here's how you set up a config file:

Line 1: Number of CPU cores (1-4)
Line 2: Scheduling algorithm (RR: round-robin, FCFS: first come first serve, SJF: shortest job first, PP: preemptive priority)
Line 3: Context switching overhead in milliseconds (100-1000)
Line 4: Time slice in milliseconds (200 - 2000) - only used for round-robin algorithm, but include in configuration file regardless
Line 5: Number of processes to run (1-24)
Lines 6 - N: (one line per process - following values separated by commas)
      PID (unique number >= 1024)
      Start time (number of milliseconds after simulator starts that process should launch: 0 - 8000)
      Number of CPU and I/O bursts (odd number: CPU bursts = I/O bursts + 1)
      CPU and I/O burst times (sequence of milliseconds: 1000 - 6000 separated by vertical pipe)
      Alternates between CPU and I/O (always starting and ending with CPU)
       Priority (number: 0 - 4)

