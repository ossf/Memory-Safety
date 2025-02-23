# Best Practices - Memory-Safe By Default Languages

While Memory-Safe by default languages are, by definition, memory-safe by default, there are ways that they can be used unsafely (or less safely). Here are best developer practices for using these languages.

## Python

TO DO

## Rust

* Use unsafe blocks sparingly and follow careful practices - see [The Rustonomicon](https://doc.rust-lang.org/nomicon/intro.html)
* When using unsafe code in Rust, the safety boundary is the module boundary. When examining snippets of unsafe code in Rust, you generally need to assess the entire module in which the unsafe code appears. [Source](https://github.com/ossf/Memory-Safety/issues/15#issuecomment-1847939439)
* Avoid using the [no_mangle](https://github.com/rust-lang/rust/issues/28179) attribute

## Go

* Using the [unsafe package](https://pkg.go.dev/unsafe#pkg-overview) is sometimes necessary when using C from Go. Be careful (TO DO: Add more about how to be careful)
* Use the [Go data race detector](https://go.dev/doc/articles/race_detector) to check for data race conditions
* Follow the [Security Best Practices for Go Developers](https://go.dev/doc/security/best-practices)

## .NET

* Use unsafe blocks sparingly and [follow guidance](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code)

## JavaScript

* Follow the [Memory management guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management)

## Java

* Avoid using `sun.misc.Unsafe` or `jdk.internal.misc.Unsafe`. If needed, prefer the newer [Foreign Function & Memory (FFM) APIs](https://docs.oracle.com/en/java/javase/22/core/foreign-function-and-memory-api.html) (Java 22 or above) which implement boundary checks when accessing off-heap memory and errors results in exceptions (e.g. IndexOutOfBoundsException) instead of crashes (e.g. SIGSEGV).
* If `sun.misc.Unsafe` or `jdk.internal.misc.Unsafe` is your only option, follow all the same best practices as you would with a [non memory-safe language](best-practice-non-memory-safe-by-default-languages.md).
* Monitor occurrences of `sun.misc.Unsafe` or `jdk.internal.misc.Unsafe` in your code (or prevent them) using for example [checkstyle's IllegalImport rule](https://checkstyle.org/checks/imports/illegalimport.html) configured to detect both `sun.*` and `jdk.internal.*`.
* If FFM APIs are used, enable the compilation option `-Xlint:restricted` to detect risky usages at compile time (the option enables warnings in the `[restricted]` log category). Similar warnings are produced by default by the JVM at runtime. These warnings should be monitored and investigated as well since they could come from third-party libraries and not just from own code.
