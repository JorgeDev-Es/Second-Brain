# Platform Implementations
The programming language (or rather, its implementations) implements to the OS.
## The OS provides the platform
The operating system is the foundational software layer that manages the computer's hardware resources. It provides a set of services and interfaces that any program running on it must use to interact with these resources.
## The language implementations uses the OS services
The compiler or interpreter for a programming language, along with its runtime and standard libraries, is built to run on top of a specific operating system. To perform tasks like opening a file, creating a thread, allocating memory, or displaying output, the language's implementation makes calls to the services provided by the OS through its API.
## The OS is the stable layer
Operating systems maintain relatively stable APIs that programs can rely on.
The OS doesn't typically change its core behavior or implement features specifically to accommodate a single programming language. It provides a general set of capabilities that various languages and applications can utilize.
## Platform-specific code
 Because different operating systems have different APIs and ways of managing resources, a programming language that aims to run on multiple platforms needs distict "implementations" for each OS. This involves writing platform-specific code within the language's runtime or standard library that knows how to use the particular OS's APIs.