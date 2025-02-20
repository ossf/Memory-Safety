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
* Use the [cxx](https://crates.io/crates/cbindgen) crate
* Monitor the Rust Foundation's [Rust/C++ interop initiative](https://github.com/rustfoundation/interop-initiative)

## Go

## .NET

## JavaScript

## Java
