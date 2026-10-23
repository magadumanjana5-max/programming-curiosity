# Garbage Collection

## Curiosity questions

20. Who cleans unused memory?
   **Answer:** The language runtime and memory allocator reclaim memory, while the operating system manages the process's overall memory resources. In CPython, reference counting reclaims many objects promptly and a cyclic garbage collector handles reference cycles.
28. What is garbage collection?
   **Answer:** Garbage collection is runtime work that finds objects a program can no longer reach and makes their memory reusable. It helps avoid manual deallocation, although it does not automatically close every external resource such as files.
29. Why doesn’t unused memory remain forever?
   **Answer:** Reclaiming unreachable objects allows a process to reuse memory for later work and reduces waste. A runtime may keep reclaimed memory in an allocator for reuse instead of immediately returning it to the operating system.
