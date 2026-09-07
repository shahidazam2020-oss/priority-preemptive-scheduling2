# ⚙️ Preemptive Priority CPU Scheduling

A Python implementation of the **Preemptive Priority Scheduling Algorithm**, an important CPU scheduling technique used in Operating Systems. This project simulates process execution, priority based preemption, and calculates essential CPU scheduling performance metrics.

---

## 📌 Project Overview

**Preemptive Priority Scheduling** is a CPU scheduling algorithm in which each process is assigned a priority. The CPU always executes the highest priority process among the processes currently in the ready queue.

In this implementation:

> **Lower priority number = Higher priority**

When a new process arrives with a higher priority than the currently running process, the CPU **preempts** the current process and starts executing the newly arrived process.

This project is developed for **educational and academic purposes** to demonstrate how CPU scheduling works internally.

---

## ✨ Features

• Preemptive priority based CPU scheduling
• Dynamic ready queue management
• Automatic process preemption
• Support for different arrival times
• Support for different burst times
• Support for different priority levels
• Completion Time calculation
• Turnaround Time calculation
• Waiting Time calculation
• Response Time calculation
• Average Waiting Time calculation
• Average Turnaround Time calculation
• Demonstration of starvation in priority scheduling
• Interactive process input through the terminal

---

## 🧠 Algorithm

The algorithm follows these main steps:

1. Read the number of processes.
2. Enter the Arrival Time, Burst Time, and Priority of each process.
3. Start execution from the earliest arriving process.
4. Check the ready queue for available processes.
5. Select the process with the highest priority.
6. If a higher priority process arrives, preempt the currently running process.
7. Continue execution until all processes are completed.
8. Calculate the scheduling performance metrics.
9. Display the final scheduling results.

### Priority Rule

| Priority Value | Meaning          |
| -------------- | ---------------- |
| `1`            | Highest Priority |
| `2`            | High Priority    |
| `3`            | Medium Priority  |
| `4`            | Low Priority     |
| `5`            | Lowest Priority  |

---

## 📊 Scheduling Metrics

The program calculates the following metrics:

### Completion Time (CT)

The time at which a process finishes execution.

### Turnaround Time (TAT)

```text
TAT = CT − AT
```

Where:

`CT` = Completion Time
`AT` = Arrival Time

### Waiting Time (WT)

```text
WT = TAT − BT
```

Where:

`TAT` = Turnaround Time
`BT` = Burst Time

### Response Time (RT)

```text
RT = First CPU Start Time − Arrival Time
```

Response Time represents how long a process waits before receiving CPU time for the first time.

---

## 🧪 Sample Input

The following processes are used to demonstrate the algorithm:

| PID | Arrival Time | Burst Time | Priority |
| :-: | -----------: | ---------: | -------: |
|  P1 |            0 |         10 |        3 |
|  P2 |            2 |          5 |        1 |
|  P3 |            4 |          3 |        4 |
|  P4 |            6 |          8 |        2 |
|  P5 |            8 |          1 |        5 |

---

## 📈 Sample Results

| PID | AT | BT | Priority | CT | TAT | WT |
| :-: | -: | -: | -------: | -: | --: | -: |
|  P1 |  0 | 10 |        3 | 23 |  23 | 13 |
|  P2 |  2 |  5 |        1 |  7 |   5 |  0 |
|  P3 |  4 |  3 |        4 | 26 |  22 | 19 |
|  P4 |  6 |  8 |        2 | 15 |   9 |  1 |
|  P5 |  8 |  1 |        5 | 27 |  19 | 18 |

### 📊 Average Performance

The program also calculates average scheduling performance, including:

**Average Waiting Time**

```text
Average WT = ΣWT / Number of Processes
```

**Average Turnaround Time**

```text
Average TAT = ΣTAT / Number of Processes
```

---

## 🔄 Example Scheduling Behavior

Consider the following situation:

```text
Time 0 → P1 starts
Time 2 → P2 arrives with higher priority
        ↓
      P1 is preempted
        ↓
      P2 executes
        ↓
Time 7 → P2 completes
        ↓
      CPU selects the next highest priority process
```

This demonstrates the main concept behind **preemptive priority scheduling**.

---

## ⚠️ Starvation

One important limitation of priority scheduling is **starvation**.

A low priority process may remain in the ready queue for a very long time if higher priority processes continuously arrive.

For example:

```text
High Priority Process
        ↓
CPU
        ↓
High Priority Process
        ↓
CPU
        ↓
High Priority Process
        ↓
CPU
        ↓
Low Priority Process
        ↓
Waiting...
```

### Possible Solution

A common solution is **aging**, where the priority of a waiting process is gradually increased over time.

---

## 📁 Project Structure

```text
priority-preemptive-scheduling2/
│
├── priority_preemptive.py
├── README.md
└── sample/
    └── sample_input.txt
```

---

## 🛠️ Technologies Used

| Technology                   | Purpose                  |
| ---------------------------- | ------------------------ |
| 🐍 Python                    | Algorithm implementation |
| 💻 Terminal                  | User input and output    |
| 🧠 Operating Systems         | CPU scheduling concepts  |
| 📊 Mathematical calculations | Performance metrics      |

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/shahidazam2020-oss/priority-preemptive-scheduling2.git
```

### 2. Navigate to the Project

```bash
cd priority-preemptive-scheduling2
```

### 3. Run the Python Program

```bash
python priority_preemptive.py
```

### 4. Enter Process Information

The program will ask you to enter:

```text
Number of processes
Process ID
Arrival Time
Burst Time
Priority
```

The program will then simulate the scheduling process and display the calculated results.

---

## 💡 Key Observations

### Higher Priority Processes

Processes with higher priority can immediately preempt processes with lower priority.

### Waiting Time

Low priority processes generally experience longer waiting times.

### Starvation

Continuous arrival of high priority processes can cause low priority processes to wait indefinitely.

### Efficient CPU Scheduling

Preemption allows the CPU to respond quickly when an important process arrives.

---

## 🎯 Learning Objectives

This project helps students understand:

• CPU scheduling fundamentals
• Process management
• Ready queue management
• Process preemption
• Priority based scheduling
• Scheduling performance metrics
• Starvation and its causes
• Operating System scheduling strategies

---

## 🔮 Future Improvements

Possible improvements for this project include:

• Add a Gantt Chart visualization
• Add non preemptive priority scheduling
• Add Round Robin scheduling
• Add Shortest Job First scheduling
• Add First Come First Serve scheduling
• Add aging to reduce starvation
• Add graphical user interface
• Export scheduling results to CSV
• Compare multiple scheduling algorithms
• Add automated test cases

---

## 📚 Related Concepts

This project is useful for studying:

```text
Operating Systems
       │
       └── CPU Scheduling
              │
              ├── FCFS
              ├── SJF
              ├── SRTF
              ├── Round Robin
              ├── Priority Scheduling
              │      └── Preemptive Priority
              └── Multilevel Queue
```

---

## 👨‍💻 Author

### Shahid Azam

**MS Computer Science | Python | Data Science | Machine Learning**

GitHub:
https://github.com/shahidazam2020-oss

---

## 📜 License

This project is intended for **educational and academic purposes**.

You are welcome to study, modify, and improve the implementation for learning purposes.

---

## ⭐ Support

If you find this project useful for learning **Operating Systems and CPU Scheduling**, consider giving the repository a ⭐ on GitHub.

**Repository:**
https://github.com/shahidazam2020-oss/priority-preemptive-scheduling2
