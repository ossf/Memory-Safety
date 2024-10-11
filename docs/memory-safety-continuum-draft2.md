# The Memory Safety Continuum

## Introduction

Over the past few years, much of the conversation around memory safety in software has treated the concept as if it were a binary. Your software is either memory safe or it is not. The truth, as is often the case, is more complex. In an ideal world, we would all write our software in memory safe by default languages, never needing to use an unsafe block or to interface with software written in a non-memory safe by default language. We do not live in that world, however, and are unlikely to live in that world in any of our lifetimes. Rather than a binary, memory safety in software should be considered a continuum. We may never be at the ideal, but we can strive to improve with every line of code we write - whether it is net new code, changes to code we are responsible for maintaining or (when appropriate) a targeted rewrite of existing code.

In the document, we present the idea of the memory safety continuum - defining various stages and helping you understand where on the continuum the software you write falls today. It is important to understand that different stages may apply to different areas of the same code base. Even if you write the majority of your software in a language like Rust, you will likely still need to interface with existing code written in C or C++, and these interfaces will require different practices for memory safety than other areas of your code base. The primary audience for this document is developers who want to write safer code. It will also likely provide value to engineering managers, product managers, project managers, and anyone else who wants to better understand memory safety in software.

### Definitions

The OpenSSF Memory Safety SIG was created with the mission of understanding and reducing memory safety vulnerabilities in Open Source Software. One of our first tasks was to define memory safety for the purposes of our group's work. We considered definitions from various sources and, ultimately, came to a consensus on [this definition](https://github.com/ossf/Memory-Safety/blob/main/docs/definitions.md). While Wikipedia may not traditionally be considered a good source to cite, the crowd editors of [the Memory safety entry](https://en.wikipedia.org/wiki/Memory_safety) have produced a comprehensive classification list of memory safety errors. Memory safety errors are the class of error that memory safe by default languages seek to eliminate.

We also came to a consensus on using the terms "memory safe by default" for languages such as Rust, Go, and C# and "non-memory safe by default" for languages such as C and C++. We feel this better reflects the complexity of achieving memory safety in software that must interact with other software.

## The Continuum

### Using Memory Safe By Default Languages

### Using Memory Safe by Default Languages to interface with Non-Memory Safe By Default Languages

### Using Non-Memory Safe By Default Languages

## Conclusion