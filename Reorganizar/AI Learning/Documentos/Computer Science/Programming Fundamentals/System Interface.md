# System Interface
Software
Applications don't directly control the computer's hardware or manage system resources like memory and processes. Instead, then interact with the operating system through well-defined interfaces called System Calls or Operating System APSs. These interfaces provide a standardized set of functions that applications can call to preform tasks like reading/writing files, creating processes, allocating memory, or interacting with network devices. This allows applications to run on different operating systems, as long as they are written to use the OS's public interfaces.


A programming language, in its raw form (like the language specification itself), doesn't typically contain the built-in instructions to directly talk to the operating system's lowest-level functions (the system calls). These system calls are the direct interface provided by the OS kernel to access hardware and manage system resources.

Instead, this interaction is handled by the **standard library** (and sometimes other runtime components) associated with that programming language. The standard library provides a set of higher-level, platform-independent functions and abstractions for common tasks.