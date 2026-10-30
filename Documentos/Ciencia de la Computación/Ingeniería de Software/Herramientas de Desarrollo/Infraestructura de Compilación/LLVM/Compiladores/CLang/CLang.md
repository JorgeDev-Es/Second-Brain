# CLang
CLang is a compiler front-end for C, C++, Objective-C, and other C-family languages. It uses LLVM as its backend and is known for its performance, diagnostics, and extensibility.

CLang is a compiler front-end built on top of LLVM. It parses C, C++, etc; code and translates it into LLVM IR.
- **Source Code (C/C++/Obj-C/Obj-C++) --> Clang --> LLVM IR --> LLVM Optimizer --> LLVM Code Generator --> Machine Code**

Clang still performs the essential steps of compilation, including assembly generation, object code creation, and linking. However, LLVM provides a more streamlined and integrated approach to these stages.