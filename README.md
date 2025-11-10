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

# 💻 OS Process Simulation: Lab Assignment 2

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
