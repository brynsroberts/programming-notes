`ps aux` is a command used in the [[Bash]] shell in [[Unix]]-like operating systems (such as [[Linux]]) to display information about the processes running on a system.

The `ps` command stands for "process status" and the `aux` options are used to display a detailed list of all processes running on the system, regardless of which user started them.

Here's a breakdown of what each part of the `ps aux` command does:

-   `ps` : This is the command to list processes.
-   `a` : This option tells the command to list processes for all users.
-   `u` : This option tells the command to display detailed information about each process.
-   `x` : This option tells the command to list processes that are not attached to a terminal.

When you run the `ps aux` command in your [[terminal]], you'll see a list of processes currently running on your system. Each [[process]] is listed with its own unique process ID (PID), the user that started the process, the CPU and memory usage of the process, and other information.