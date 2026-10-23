# Rabbit Hole 2: What Happens When You Run Code?

**Question:** When I type `python app.py`, what happens between pressing Enter and seeing the output?

**Answer:** The shell parses the command and asks the operating system to start the Python executable. Python reads and parses `app.py`, compiles it to internal code objects (CPython normally uses bytecode), and executes them in its runtime. The program may print output, access files, or make network requests. When it finishes, the process returns an exit status; an unhandled error can stop it early.

- **WHY:** The operating system needs an executable process to run instructions and manage resources.
- **WHAT:** The command starts a Python runtime and gives it a script filename.
- **HOW:** Shell lookup, process creation, source parsing, code execution, and output handling happen in sequence.
- **WHERE:** The Python process runs on the computer where the command was executed, unless the shell is connected to a remote machine or container.
- **WHEN:** Parsing and execution begin after the process starts; importing modules and I/O add more steps.
- **WHO:** The shell, operating system, Python runtime, and program code each play a role.
- **WHAT IF:** A missing executable, syntax error, unhandled exception, or resource failure produces an error or non-zero exit status.

Continue with [how programs run](../03-how-programs-run/compiler.md), [processes](../03-how-programs-run/process.md), and [the interpreter](../03-how-programs-run/interpreter.md).
