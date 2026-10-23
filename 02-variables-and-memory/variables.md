# Your First Line of Code

## Curiosity questions

11. What happens internally when you write `x = 10`?
   **Answer:** In Python, the runtime obtains an integer object representing `10` and binds the name `x` to it in the current scope. Assignment changes a name-to-object binding; it is not a command to reserve a permanent physical slot called `x`.
12. Where is `10` stored?
   **Answer:** The integer is represented by an object in the Python process's memory, typically RAM while the process runs. The operating system manages the process's virtual address space and maps it to physical memory as needed.
13. Where is `x` stored?
   **Answer:** `x` is a name in a namespace, such as a module, local scope, or object attribute, and that namespace refers to the integer object. The exact internal representation depends on the Python implementation and scope.
14. Is `x` actually the value `10`?
   **Answer:** Conceptually, `x` is a name referring to an object whose value is 10. This distinction matters because multiple names can refer to the same object, especially mutable objects.
15. What happens when you write `x = 10` and then `x = 20`?
   **Answer:** The name `x` is first bound to the integer object `10`, then rebound to `20`. Integers are immutable, so the object `10` is not modified; other references to it remain valid.
16. What happens to `10`?
   **Answer:** If no live reference points to the `10` object, it becomes eligible for reclamation. Python implementations manage that memory; the precise time memory is reclaimed is not guaranteed by the language.
17. What happens when you write `a = b = c = 100`?
   **Answer:** Python evaluates the right-hand value and binds each name to that object. Since integers are immutable, sharing the same object is safe; code should not rely on object identity for numeric values.
18. Are `a`, `b` and `c` three copies of `100`?
   **Answer:** They are three names bound to the value 100, and an implementation may let them refer to the same integer object. Integer identity and object reuse are implementation details; compare numeric values with `==`, not `is`.
19. What happens to variables when a function finishes?
   **Answer:** The function's local namespace normally becomes unreachable when the call ends, so its local names cease to be available. Objects referenced elsewhere remain alive; unreferenced objects can be reclaimed by the runtime.
