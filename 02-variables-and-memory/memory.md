# Memory — The Hidden World

## Curiosity questions

21. What is RAM actually doing while your program runs?
   **Answer:** RAM holds the program's currently needed instructions and data so the processor can access them quickly. The operating system gives each process a virtual address space and manages the mapping to physical memory.
22. What is the difference between RAM and storage?
   **Answer:** RAM is fast working memory that is generally volatile: its contents are lost when power is off. Storage such as an SSD keeps files and databases persistently, but is usually slower; programs load data from storage into memory to work on it.
23. Where does a Python variable live?
   **Answer:** A Python variable is a name binding in a namespace, not a labeled physical cell. Its namespace and the object it references are represented in the Python process's memory, with details varying by Python implementation.
24. What is a memory address?
   **Answer:** It is a location identifier used to access data in an address space. Modern programs usually see virtual addresses, which the operating system and hardware translate; they need not correspond directly to physical RAM locations.
25. Why can’t we normally see memory addresses in Python?
   **Answer:** Python abstracts memory management to make programs easier and safer to write. Low-level addresses are implementation-specific and unstable; tools such as `id()` expose an identity value, but Python does not promise it is a physical memory address.
30. What happens when your program consumes too much memory?
   **Answer:** The operating system may swap some memory to storage, slow the machine, or terminate the process; a Python allocation can also fail with `MemoryError`. The remedy is to reduce live data, stream or batch work, or provide more appropriate resources.
