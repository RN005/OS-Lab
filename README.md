# 💻 OS-Lab (ENCS351)
# Linux Process Management 

This repository contains Python programs implementing core **Linux Process Management** concepts using the **`os`** and **`subprocess`** modules.

## Experiment Tasks

| Task | Focus | Key Concept | Description |
| :--- | :--- | :--- | :--- |
| **Task 1** | **Process Creation** | `fork()`, `wait()` | Create multiple children with `os.fork()` and ensure the parent waits for all with `os.waitpid()`. |
| **Task 2** | **Command Execution** | `fork()`, `execvp()` | Child process uses **`os.execvp()`** to replace itself and execute external commands (e.g., `ls -l`). |
| **Task 3** | **Zombie & Orphan** | Process States | Code to intentionally create and demonstrate both **Zombie** (unreaped child) and **Orphan** (parent exits early) process states. |
| **Task 4** | **`/proc` Inspection** | `/proc` Filesystem | Read and display live process details (Name, State, Executable, FDs) by parsing the Linux **`/proc`** filesystem. |
| **Task 5** | **Process Prioritization** | `nice()` Value | Create CPU-intensive children and apply different **`os.nice()`** values to observe the scheduler's impact on execution time. |
