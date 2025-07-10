# Best Practices - Interfacing Between Memory-Safe By Default and Non-Memory-Safe by Default Languages

While new software is increasingly being written in memory safe by default languages, there are billions of existing lines of code written in non-memory safe by default languages. Targeted rewrites of highly used, highly vulnerable software components may be necessary and beneficial to the safety of the Open Source ecosystem, but we do not advocate for mass rewrites of all existing code written in non-memory safe by default languages.

It is and will continue to be necessary for software written in memory safe by default languages to interact with software written in non-memory safe by default languages through foreign function interfaces (FFI). FFI is one of the primary uses for unsafe blocks within memory safe-by-default languages (for example Rust).

## General

* separate all FFIs into a separate crate/module/package so that it can be audited in isolation. All exported symbols from that crate/module/package should be memory safe. [Source](https://github.com/ossf/Memory-Safety/issues/36#issuecomment-2477083785)

## Python

## Rust

* Follow [Foreign Function Interface guidance in The Rustnomicon](https://doc.rust-lang.org/nomicon/ffi.html)
* Use the [bindgen](https://crates.io/crates/bindgen) crate
* Use the [cbindgen](https://crates.io/crates/cbindgen) crate
* Use the [cxx](https://crates.io/crates/cxx) crate
* Monitor the Rust Foundation's [Rust/C++ interop initiative](https://github.com/rustfoundation/interop-initiative)

## Go

* Go is itself a memory safe language as long as you don't use the unsafe package. The [rules for using the unsafe package safely](https://pkg.go.dev/unsafe) explain the requirements, particularly in the description of the Pointer type.

* Go interacts with other languages using a tool called cgo. The [rules for passing pointers](https://pkg.go.dev/cmd/cgo#hdr-Passing_pointers) provide the details.

## .NET

## JavaScript

## Java

* Avoid using the legacy Java Native Interface (JNI) APIs. If needed, prefer the newer Foreign Function & Memory (FFM) APIs introduced in Java 22.
* Monitor or prevent JNI API occurrences (e.g. uses of the `native` keyword or calls to `System.load()` or `System.loadLibrary()`) in your code using [static code analysis tools](https://www.baeldung.com/tag/static-analysis).
* If using JNI is your only option, follow all the same best practices as you would with a [non memory-safe language](best-practice-non-memory-safe-by-default-languages.md).
* Always enable the [-Xcheck:jni JVM option](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/clopts002.html#CHDHCBBG) to activate additional validation of JNI functions' arguments. Even if your code does not use JNI, your third-party dependencies might (JDBC drivers are a common example).
* The [-verbose:jni JVM option](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/clopts002.html#CHDCHGEE) can also be useful to detect or troubleshoot JNI issues but beware of the potential performance as it could cause a lot of extra log messages if JNI is heavily used in your application.
