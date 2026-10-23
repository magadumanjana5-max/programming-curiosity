# Running `python app.py`

## Curiosity questions

31. Who receives the `python app.py` command?
   **Answer:** The command shell parses the command and asks the operating system to locate and start the `python` executable with `app.py` as an argument. The launched Python runtime then handles the script.
32. How does the operating system know where Python is?
   **Answer:** A shell typically searches the directories listed in the `PATH` environment variable, unless you specify a path. The operating system loads the executable found there; virtual environments can place a different Python earlier in `PATH`.
36. How does Python read your `.py` file?
   **Answer:** The Python runtime opens the file, decodes its source text, parses it, and compiles it to code objects, usually using bytecode internally. It then executes those code objects; exact caching and compilation behavior depends on the implementation.
37. Does Python directly understand your source code?
   **Answer:** Not as raw text at the processor level. The Python implementation parses the source and executes its meaning through a runtime, which may compile it to bytecode or machine code internally.
38. What is bytecode?
   **Answer:** Bytecode is a compact set of virtual-machine instructions produced from source code. CPython executes its bytecode with the Python Virtual Machine; bytecode is not the same as native processor instructions and may vary between versions or implementations.

## Rabbit hole

- [What happens between pressing Enter and seeing program output?](../10-rabbit-holes/what-happens-when-you-run-code.md)
