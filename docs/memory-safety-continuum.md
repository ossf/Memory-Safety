# Memory Safety Continuum

At this SIG's January 25, 2024 meeting, we discussed the idea of a continuum when it comes to software memory safety.

When discussing memory safety, it's easy to fall into the idea of a memory safety binary - either your software is "memory safe" or it is not. When considering reality - especially with re: to so much existing software (legacy or not) - it is more nuanced.

This DRAFT document lays out the idea of the "Memory Safety Continuum". Eventually, this idea may be used as a foundation for other content which will help developers and organizations identify where they are on the continuum and how to get to where they want to be.

## What is Memory Safety?

Rather than using terms like "Memory Safe Language" and "Memory Unsafe Language", this SIG prefers the terms "memory safe by default" and "non-memory safe by default". Please see our [useful definitions](definitions.md) file for more information about memory safety and undefined behavior.

## The Continuum

This is a very rough idea of what the continuum might look like - from "least safety" to "most safety"

* Using a non-memory safe by default language (such as C or C++) without any developer best practices or automated tooling to check for memory safety
* Using a non-memory safe by default language with developer best practices, but no automated tooling to check for memory safety
* Using a non-memory safe by default language with developer best practices and automated tooling to check for memory safety
* Using a memory safe by default language (such as Rust, Go, Python, Java, JavaScript, C#) without developer best practices and automated tooling
* Using a memory safe by default language with developer best practices
* Using a memory safe by default language with developer best practices and automated tooling

### Using a non-memory safe by default language without an developer best practies or automated tooling

Using raw C or C++ (or old versions of C and C++ language and compiler)

### Using a non-memory safe by default language with developer best practices, but no automated tooling

Examples:

* [Using attributes such as `cleanup` and classes when writing C](https://lwn.net/Articles/934679/) (and depending on developers to manually check this) 
* Following the [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines) when writing C++
* Using the [C++ Compiler Hardening Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides) when compiling C++ code

### Using a non-memory safe by default language with developer best practices and automated tooling

TO DO

### Using a memory safe by default language without developer best practices or automated tooling

Examples:

* Using unsafe blocks in Rust [without assessing the entire module in which the unsafe code appears](https://github.com/ossf/Memory-Safety/issues/15#issuecomment-1847939439)
* Using the [no_mangle](https://github.com/rust-lang/rust/issues/28179) attribute in Rust

### Using a memory safe by default language with developer best practices, but no automated tooling

Examples:

* Following the [Rustnomicon](https://doc.rust-lang.org/nomicon/intro.html) careful practices when using unsafe blocks in Rust
* Following best practices (LINK NEEDED) when using the Go [unsafe](https://pkg.go.dev/unsafe#pkg-overview) package
* Following [Javascript Memory Management](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management) practices

### Using a memory safe by default language with developer best practices and automated tooling

Examples:

* Using the [Go Data Race Detector](https://go.dev/doc/articles/race_detector)
* Using other tools such as [govulncheck, fuzzing, and vet](https://go.dev/doc/security/best-practices) when writing Go code

## FAQ

### Why do you rank using automated tooling higher than just using developer best practices?

The amount software that has already been produced is staggering - and it is only growing every day. Expecting every developer to manually check their code (and the code their code interacts with) is no longer practical or possible. Automated tooling must be used to catch (at the least) known, common vulnerabilities that a developer may unintentionally introduce in their code.
