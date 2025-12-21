# Advanced CPU Scheduling Algorithms: Preemptive Priority Scheduling
## Overview
This repository contains an implementation of Preemptive Priority Scheduling, one of the advanced CPU scheduling algorithms used in operating systems. The project demonstrates how processes are scheduled based on priority, with preemption ensuring that higher-priority tasks interrupt lower-priority ones.
The implementation is designed for educational purposes and includes:

Complete source code in Python.
Sample input dataset for testing.
Calculation of key performance metrics such as:

Completion Time (CT)
Turnaround Time (TAT)
Waiting Time (WT)
Response Time (RT)
## Features
Accurate simulation of ready queue management and preemption checks.
Dynamic calculation of average Waiting Time and Turnaround Time.
Handles multiple processes with varying arrival times, burst times, and priorities.
Demonstrates potential issues like starvation in priority-based scheduling.
## Algorithm Summary
Preemptive Priority Scheduling works by:
Assigning each process a priority (lower number = higher priority).
Continuously checking for arriving processes and preempting the current process if a higher-priority process arrives.
Computing scheduling metrics after all processes complete.
## Sample Input
PID   Arrival TimeBurstTime   Priority
P1       0        10             3
P2       2        5              1
P3       4        3              4
P4       6        8              2
P5       8        1              5
## Results
PID      AT       BT
p1       0        10
p2       2        5
p3       4        3
p4       6        8
p5       8        1
## How to Run
1. Clone the repository:
   1 git clone https://github.com/shahidazam2020-oss/priority-preemptive-scheduling2.git
2. Navigate to the project directory:
   1 cd priority-preemptive-scheduling2
3. Run the Python script:
   1 python priority_preemptive.py
4. Enter the number of processes and their details when prompted.
## Key Observations
Higher-priority processes preempt lower-priority ones immediately.
Lower-priority processes experience longer waiting times.
Preemptive priority scheduling can lead to starvation for low-priority tasks.
## Repository Links
https://github.com/shahidazam2020-oss/priority-preemptive-scheduling2.git
