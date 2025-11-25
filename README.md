# 💻 OS-Lab (ENCS351)
# 1. Linux Process Management 

This repository contains Python programs implementing core **Linux Process Management** concepts using the **`os`** and **`subprocess`** modules.

## Experiment Tasks

| Task | Focus | Key Concept | Description |
| :--- | :--- | :--- | :--- |
| **Task 1** | **Process Creation** | `fork()`, `wait()` | Create multiple children with `os.fork()` and ensure the parent waits for all with `os.waitpid()`. |
| **Task 2** | **Command Execution** | `fork()`, `execvp()` | Child process uses **`os.execvp()`** to replace itself and execute external commands (e.g., `ls -l`). |
| **Task 3** | **Zombie & Orphan** | Process States | Code to intentionally create and demonstrate both **Zombie** (unreaped child) and **Orphan** (parent exits early) process states. |
| **Task 4** | **`/proc` Inspection** | `/proc` Filesystem | Read and display live process details (Name, State, Executable, FDs) by parsing the Linux **`/proc`** filesystem. |
| **Task 5** | **Process Prioritization** | `nice()` Value | Create CPU-intensive children and apply different **`os.nice()`** values to observe the scheduler's impact on execution time. |

# 💻 Process Simulation

This project is a Python-based simulation of a simplified **Operating System Process Lifecycle**, designed for the **Operating Systems Lab Assignment 2**.  
It demonstrates how an OS manages process creation, execution, and termination using Python’s built-in multiprocessing capabilities.

---

## 🧩 Project Summary

| Aspect | Details |
|--------|----------|
| 🎯 **Goal** | Simulate a basic Operating System's process management lifecycle. |
| 🛠️ **Technology** | Python 3.x with `multiprocessing` and `logging` modules. |

## ✨ Key Features

### 🚀 Initialization Flow
- Simulates **system startup** and **graceful shutdown**.
- Displays logs for each stage of the simulation.

### ⚙️ Concurrency
- Creates and executes **multiple concurrent child processes** using `multiprocessing.Process`.
- Each process performs a **dummy task** to simulate workload.

### ✅ Process Management
- Utilizes `p.join()` to ensure the **parent process waits** for all child processes to terminate properly.
- Handles process lifecycle: **creation → execution → completion**.

### 📜 System Logging
- Maintains a structured log file `process_log.txt` that records:
  - Process start time
  - Process end time
  - Process name and PID
- Mimics **OS kernel-level logging** for educational purposes.

# 💾 Operating Systems Lab 3: Memory and File Allocation Strategies

This Jupyter Notebook simulates essential memory management and file allocation techniques used in Operating Systems using Python.

---

## 🚀 Tasks Overview

| Task | Title | Concepts Covered | Allocation Strategy |
| :--- | :--- | :--- | :--- |
| **Task 1** | CPU Scheduling with Gantt Chart | Priority scheduling, WT and TAT calculation | Priority Scheduling |
| **Task 2** | Sequential File Allocation | Allocate file blocks contiguously on disk | Sequential |
| **Task 3** | Indexed File Allocation | File block allocation using an index block | Indexed |
| **Task 4** | Contiguous Memory Allocation | First Fit, Best Fit, Worst Fit algorithms | First/Best/Worst Fit |
| **Task 5** | MFT & MVT Memory Management | Fixed vs Variable memory partitions | MFT / MVT |

---

## 🗂️ Key Concepts Simulated

### **Sequential File Allocation**
- Entire file stored in a single continuous block of disk space.

### **Indexed File Allocation**
- Uses an index block to store addresses of all file blocks.
- Allows non-contiguous storage.

### **MFT (Multiprogramming with Fixed Tasks)**
- Memory is divided into fixed-size partitions.
- Processes must fit these partitions.
- May cause **internal fragmentation**.

### **MVT (Multiprogramming with Variable Tasks)**
- Partitions created dynamically based on process size.
- Minimizes internal fragmentation.

### **Contiguous Allocation Strategies**
- **First Fit:** Assign first sufficiently large block.
- **Best Fit:** Assign smallest available suitable block.
- **Worst Fit:** Assign largest available block.

---

## ⚙️ How to Run

1. Ensure you have a Python environment capable of running Jupyter Notebooks.
2. Open `Lab_3.ipynb` in Jupyter or VS Code.
3. Run the notebook cells sequentially.
4. Provide inputs (file sizes, process sizes, blocks, etc.) when prompted.

---

## 📁 File Information

- **Filename:** `Lab_3.ipynb`
- **Category:** Operating Systems Lab
- **Topics:** Memory allocation, file systems, scheduling

# 💻 Operating Systems Lab 4: Process Management and CPU Scheduling

This Jupyter Notebook contains Python-based simulations demonstrating core Operating Systems concepts such as process management, inter-process communication (IPC), virtual machine detection, and CPU scheduling.

---

## 🚀 Tasks Overview

| Task | Title | Concepts Covered | Python Modules Used |
| :--- | :--- | :--- | :--- |
| **Task 1** | Batch Processing Simulation | Sequential execution of scripts | `subprocess` |
| **Task 2** | System Startup and Logging | Multiprocessing, boot/shutdown simulation, logging | `multiprocessing`, `logging`, `time` |
| **Task 3** | System Calls and IPC | Inter-Process Communication using `Pipe` | `multiprocessing.Process`, `multiprocessing.Pipe` |
| **Task 4** | VM Detection and Shell Interaction | Checking system characteristics to detect a virtual machine | `os`, `platform`, `subprocess` |
| **Task 5** | CPU Scheduling Algorithms | WT & TAT for FCFS, SJF, Priority, Round Robin | *(Standard Python)* |

---

## 🧮 Task 5: CPU Scheduling Algorithms

This section includes implementations of the following **non-preemptive scheduling algorithms**:

- **First-Come, First-Served (FCFS)**
- **Shortest Job First (SJF)**
- **Priority Scheduling** (lower number = higher priority)
- **Round Robin** (time quantum)

The notebook calculates:

- **Waiting Time (WT)**
- **Turnaround Time (TAT)**

for each process based on user-provided burst times and priorities.

---

## ⚙️ How to Run

1. Ensure Python is installed with the standard library modules:
   - `subprocess`, `multiprocessing`, `logging`, `time`, `platform`
2. Open the notebook in Jupyter or VS Code.
3. Run each cell sequentially to execute all tasks.

---

## 📁 File Information

- **Filename:** `Lab_4.ipynb`
- **Category:** Operating Systems Lab
- **Topics:** Processes, IPC, VM detection, Scheduling

