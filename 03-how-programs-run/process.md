# Process

## Curiosity questions

33. What is a process?
   **Answer:** A process is a running program instance with its own virtual address space and operating-system-managed resources, such as open files. A process can contain one or more threads and is isolated from other processes to a degree enforced by the OS.
40. What happens when the program crashes?
   **Answer:** An unhandled error or fatal fault can terminate the process, often with an error message or non-zero exit status. The operating system reclaims its resources; a supervisor may detect the exit and restart it, but unsaved in-memory work can be lost.

## Rabbit hole

- [How does a program know that another program has crashed?](../10-rabbit-holes/how-does-a-program-detect-a-crash.md)
