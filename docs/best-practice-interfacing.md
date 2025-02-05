While new software is increasingly being written in memory safe by default languages, there are billions of existing lines of code written in non-memory safe by default languages. Targeted rewrites of highly used, highly vulnerable software components may be necessary and beneficial to the safety of the Open Source ecosystem, but we do not advocate for mass rewrites of all existing code written in non-memory safe by default languages.

It is and will continue to be necessary for software written in memory safe by default languages to interact with software written in non-memory safe by default languages through foreign function interfaces (FFI). FFI is one of the primary uses for unsafe blocks within Rust (as well as within other languages).

## Python

## Rust 

* Following [Foreign Function Interface guidance in The Rustnomicon](https://doc.rust-lang.org/nomicon/ffi.html)
* Use the [bindgen](https://crates.io/crates/bindgen) crate
* Use the [cbindgen](https://crates.io/crates/cbindgen) crate
* Use the [cxx](https://crates.io/crates/cbindgen) crate
* Monitor the Rust Foundation's [Rust/C++ inerop initiative](https://github.com/rustfoundation/interop-initiative)

## Go

## .NET

## JavaScript

## Java