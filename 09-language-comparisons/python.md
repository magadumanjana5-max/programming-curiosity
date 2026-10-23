# Python

## Curiosity questions

81. Why is Python popular for AI?
   **Answer:** Python is approachable and has a large ecosystem for data processing, scientific computing, and machine learning. Many heavy computations run in optimized native libraries or on GPUs, so Python's own execution speed is often not the main bottleneck.
87. Is Python actually slower than Java?
   **Answer:** For many CPU-bound tasks, standard Python implementations such as CPython execute ordinary code more slowly than optimized Java on the JVM. Real results depend on workload, libraries, I/O, and runtime warm-up; a benchmark must compare equivalent work.
89. Can Python call code written in C?
   **Answer:** Yes. Python can use C through extension modules, the Python C API, or foreign-function interfaces such as `ctypes` and `cffi`. This is useful for native libraries and performance-critical work, but requires care around data representation, memory ownership, and platform compatibility.
