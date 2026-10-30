# Input/Output
A program's core logic is typically self-contained. It performs computations based on the data it has. However, for a program to be useful, is almost always needs to interact with the world outside its own execution environment. This interaction is broadly categorized as Input/Output (I/O).

I/O is the mechanism by which a program receives data from or sends data to external sources. These external sources can be:

1. **Users:** Interacting through a command line interface (CLI), a graphical user interface (GUI), or other human interface devices (like keyboards, mice, microphones, screens).
2. **Files:** Reading configuration, data, or source code; writing results, logs, or new data.
3. **Other Programs:** Communicating through various mechanisms like pipes, sockets (network I/O), shared memory, or by loading libraries (like DLLs) and calling their functions.
4. **Devices:** Interacting with hardware like printers, sensors, or network interfaces.
While the compiled `.exe` or executable file contains the program's instructions, it relies on the **operating system (OS)** and **standard libraries** (provided with the programming language or the OS) to perform these I/O operations. The OS manages resources like files, devices, and network connections, and provides system calls that programs use to request I/O operations. Standard libraries wrap these system calls in more convenient, high-level functions that programmers can easily use.