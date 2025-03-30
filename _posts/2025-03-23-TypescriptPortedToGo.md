---
title: The Microsoft porting Typescript to Go
tags: Typescript Go
---

It was announced that the TypeScript compiler, which is based on JavaScript, will be ported from MS to Go.
The main goal of the project is to port the existing codebase for as compatible as possible.

#### Main features
- Build time reduced to less than 1/10
    - 3.3x at native(compile language), 3.3x at concurrency
- EditorSpeed
- Reduced memory usage
- Simple Deployment

#### Why Go?
[Anders Hejlsberg's comment](https://github.com/microsoft/typescript-go/discussions/411) : "The TypeScript compiler's move to Go was influenced by specific technical requirements, such as the need for structural compatibility with the existing JavaScript-based codebase, ease of memory management, and the ability to handle complex graph processing efficiently. After evaluating numerous languages and making multiple prototypes — including in C# — Go emerged as the optimal choice, providing excellent ergonomics for tree traversal, ease of memory allocation, and a code structure that closely mirrors the existing compiler, enabling easier maintenance and compatibility."

Typescript requires automatic garbage collection and support for cyclic graphs, while avoiding incompatibilities and unpredictable behavior.
Rust was not chosen due to its handling of cyclic data structures (like ASTs with child and parent pointers and recursive elements).
Using Rust would require a complete rewrite rather than a straightforward port of these features.
They needed a language that provides excellently optimized native code across all platforms, supporting automated garbage collection, shared memory concurrency, cyclic data structures, and inline data structures.

#### Main usages Concurrency

Parse and bind operations(Tokenization, Syntax Analysis) - were the easiest to optimize, achieving 3-4 times faster performance.
Many of these improvements will be realized once shared memory support is implemented.
Type checking now uses 20% less memory and runs 3.3 times faster.
But, There were concurrency problems with type checker operations in multithreaded environments.
Type checkers begin their checks under an immutable AST.
The solution divides each source file in the project into quarters and runs four type checkers concurrently.
Each type checker processes the whole project but handles only its assigned quarter of files.
While this approach may generate duplicate types, the performance trade-off is worth it. Anders Hejlsberg said “That’s a great bargain.”
[TypeScript is being ported to Go | interview with Anders Hejlsberg - Michigan TypeScript](https://youtu.be/10qowKUW82U?si=QVk7RZA_XssoItNV&t=2522)

#### Communication with Other Languages
- Language-neutral binding (primarily using Language Server Protocol)
- Currently exploring solutions to create richer and synchronous APIs in this area

#### Negative Opinion
- TypeScript is no longer a superset of JS.
- Disappointment at not porting to C# with handling many of the issues in C#.

#### References
- https://devblogs.microsoft.com/typescript/typescript-native-port/
- https://github.com/microsoft/typescript-go/discussions/categories/faqs
- https://github.com/microsoft/typescript-go/discussions/411
- https://www.youtube.com/watch?v=10qowKUW82U
- https://en.wikipedia.org/wiki/Abstract_syntax_tree
- https://en.wikipedia.org/wiki/Ahead-of-time_compilation
- https://en.wikipedia.org/wiki/Just-in-time_compilation