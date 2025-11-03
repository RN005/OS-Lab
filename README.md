# OS-Lab
Task,Focus,Description,Key Concept
Task 1,Process Creation,Create multiple children with os.fork() and ensure parent waits for all with os.waitpid().,"fork(), wait()"
Task 2,Command Execution,"Child process uses os.execvp() to replace itself and execute external commands (e.g., ls -l).","fork(), execvp()"
Task 3,Zombie & Orphan,Code to intentionally create and demonstrate both Zombie (unreaped child) and Orphan (parent exits early) process states.,Process States
Task 4,/proc Inspection,"Read and display live process details (Name, State, Executable, FDs) by parsing the Linux /proc filesystem.",/proc Filesystem
Task 5,Process Prioritization,Create CPU-intensive children and apply different os.nice() values to observe the scheduler's impact on execution time.,nice() Value
