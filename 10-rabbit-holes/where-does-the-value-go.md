# Rabbit Hole 1: Where Does the Value Go?

**Question:** When I type `x = 10`, where exactly does `10` go?

**Answer:** Python evaluates `10` as an integer object and binds the name `x` to that object in the current namespace. The object and namespace are represented in the Python process's virtual memory, which the operating system maps to physical RAM as needed. `x` is not a permanent physical box, and Python does not promise a particular address or storage layout.

**Follow the trail:** `name → object → process memory → virtual memory → physical RAM`

- **WHY:** Names make values easier to use and change without manually managing addresses.
- **WHAT:** `10` is an integer object; `x` is a name bound to it.
- **HOW:** The Python runtime creates or reuses an integer object and records a name binding.
- **WHERE:** The binding and object exist within the process's memory.
- **WHEN:** The object can be reclaimed when no references keep it reachable; exact timing depends on the implementation.
- **WHO:** Python manages objects and the operating system manages process memory.
- **WHAT IF:** If the process runs out of memory, allocation can fail or the operating system may terminate it.

Explore [variables](../02-variables-and-memory/variables.md), [memory](../02-variables-and-memory/memory.md), and [stack and heap](../02-variables-and-memory/stack-and-heap.md).
