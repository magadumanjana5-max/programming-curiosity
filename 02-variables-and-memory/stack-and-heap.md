# Stack and Heap

## Curiosity questions

26. What is a stack?
   **Answer:** A call stack tracks active function calls and their execution context, such as return locations and local bookkeeping. Calls usually add frames and returns remove them; stack limits help detect excessive recursion.
27. What is a heap?
   **Answer:** The heap is a general area used for dynamically managed objects whose lifetimes are not simply tied to one function call. In Python, most objects are dynamically allocated, but exact stack-versus-heap behavior is an implementation detail rather than a Python language guarantee.
