# Best Practices - Non Memory-Safe By Default Languages

This working group recommends using a memory-safe by default language whenever possible or practical. However, when using a memory-safe by default language is not possible or practical, there are developer practices that will improve memory safety, even if it is not the default.

## Language independent guidelines

* Chromium is using the [rule of 2](https://chromium.googlesource.com/chromium/src/+/master/docs/security/rule-of-2.md) to improve security. This involves sandboxing unsafe code that processes untrusted input.

## C

* [Scope-based resource management for the kernel](https://lwn.net/Articles/934679/)

## C++

* [Google's whitepaper](https://research.google/pubs/secure-by-design-googles-perspective-on-memory-safety/) summarizes most of the security mitigations they have in place for C++ including sanitizers, fuzzing, guidelines, and static analysis.
* Microsoft's [response](https://learn.microsoft.com/en-us/cpp/code-quality/build-reliable-secure-programs) to NISTIR 8397 summarizes best practices to build reliable and secure C++ programs for the Windows platform.
* Apple's [Secure Coding Guide](https://developer.apple.com/library/archive/documentation/Security/Conceptual/SecureCodingGuide/Introduction.html) includes generic advices for C, C++ and Objective C, as well as some platform specific guidelines.
* The [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) is a collection of best practices to write better and safer C++.
* The [C/C++ Hardening Guide](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++.html) discusses what compiler options to use to mitigate the risks of vulnerabilities getting exploited.
