# Best Practices - Memory-Safe By Default Languages

While Memory-Safe by default languages are, by definition, memory-safe by default, there are ways that they can be used unsafely (or less safely). Here are best developer practices for using these languages.

## Python

TO DO

## Rust

* Use unsafe blocks sparingly and follow careful practices - see [The Rustonomicon](https://doc.rust-lang.org/nomicon/intro.html)
* When using unsafe code in Rust, the safety boundary is the module boundary. When examining snippets of unsafe code in Rust, you generally need to assess the entire module in which the unsafe code appears. [Source](https://github.com/ossf/Memory-Safety/issues/15#issuecomment-1847939439)
* Avoid using the [no_mangle](https://github.com/rust-lang/rust/issues/28179) attribute
* Use [cargo-geiger](https://github.com/geiger-rs/cargo-geiger) to monitor statistics about a crate's use of unsafe code

## Go

* Use the [unsafe package](https://pkg.go.dev/unsafe#pkg-overview) is sometimes necessary when using C from Go. Be careful (TO DO: Add more about how to be careful)
* Use the [Go data race detector](https://go.dev/doc/articles/race_detector) to check for data race conditions
* Follow the [Security Best Practices for Go Developers](https://go.dev/doc/security/best-practices)

## .NET

* Use unsafe blocks sparingly and [follow guidance](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code)

## JavaScript

* Follow the [Memory management guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management)

## Java

TO DO
