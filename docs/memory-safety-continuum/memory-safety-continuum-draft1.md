# Memory Safety Continuum

At this SIG's January 25, 2024 meeting, we discussed the idea of a continuum when it comes to software memory safety.

When discussing memory safety, it's easy to fall into the idea of a memory safety binary - either your software is "memory safe" or it is not. When considering reality - especially with re: to so much existing software (legacy or not) - it is more nuanced.

This DRAFT document lays out the idea of the "Memory Safety Continuum". Eventually, this idea may be used as a foundation for other content which will help developers and organizations identify where they are on the continuum and how to get to where they want to be.

## Audience

The audience for this draft is developers - however, the audience may expand with future drafts/versions of this document.

## What is Memory Safety?

Rather than using terms like "Memory Safe Language" and "Memory Unsafe Language", this SIG prefers the terms "memory safe by default" and "non-memory safe by default". Please see our [useful definitions](definitions.md) file for more information about memory safety and undefined behavior.

## The Continuum - Understanding Where Your Software Is Now

This continuum, from "most safe" to "least safe", is intended to help you define and understand the memory safety of your software and what you can do to improve it. We propose that developers and organizations should use modern toolchains and follow current best practices for their software ecosystems. In particular, whenever, there is a memory safe feature or workflow, it should be adopted over a non-memory safe variant.

- Using a memory safe by default language (such as Rust, Go, Python, Java, JavaScript, C#), following the language's best practices that include using language processors and additional automated tooling to check for memory safety in your code as well as in all your dependencies' code ([examples](#using-a-memory-safe-by-default-language-with-developer-best-practices-and-automated-tooling-to-check-for-memory-safety-in-your-code-as-well-as-in-all-dependencies-code))
- Using a memory safe by default language, following the language's best practices that include using language processors and additional automated tooling to check for memory safety in your code only ([examples](#using-a-memory-safe-by-default-language-with-developer-best-practices-language-processors-post-processors-etc-and-automated-tooling-to-check-for-memory-safety-in-your-code))
- Using a memory safe by default language, following the language's best practices that include using language processors without any additional tooling ([examples](#using-a-memory-safe-by-default-language-with-developer-best-practices-and-language-processors-post-processors-etc-but-no-automated-tooling))
- Using a memory safe by default language without following the language's best practices ([examples](#using-a-memory-safe-by-default-language-without-developer-best-practices))
- Using a non-memory safe by default language (such as C or C++), following the language's best practices that include using language processors and additional automated tooling to check for memory safety in your code as well as in all your dependencies' code ([examples](#using-a-non-memory-safe-by-default-language-with-developer-best-practices-and-automated-tooling-to-check-for-memory-safety-in-your-code-as-well-as-in-all-your-dependencies-code))
- Using a non-memory safe by default language, following the language's best practices that include using language processors and additional automated tooling to check for memory safety in your code only ([examples](#using-a-non-memory-safe-by-default-language-with-developer-best-practices-and-automated-tooling-to-check-for-memory-safety-in-your-code))
- Using a non-memory safe by default language, following the language's best practices that include using language processors without any additional tooling ([examples](#using-a-non-memory-safe-by-default-language-with-developer-best-practices-but-no-automated-tooling))
- Using a non-memory safe by default language, without following the language's best practices ([examples](#using-a-non-memory-safe-by-default-language-without-developer-best-practies-or-automated-tooling))

### Examples

#### Using a memory safe by default language with developer best practices and automated tooling to check for memory safety in your code as well as in all dependencies' code

- Using a fuzzer such as [AFL++](https://github.com/AFLplusplus/AFLplusplus) on both your own code and third party code
- TO DO - add more examples

#### Using a memory safe by default language with developer best practices, language processors, post processors etc. and automated tooling to check for memory safety in your code

- Using the [Go Data Race Detector](https://go.dev/doc/articles/race_detector)
- Using other tools such as [govulncheck, fuzzing, and vet](https://go.dev/doc/security/best-practices) when writing Go code
- Using a mutation tester such as [cargo-mutants](https://github.com/sourcefrog/cargo-mutants)
- Using [CodeQL](https://codeql.github.com/) for the [languages that CodeQL supports](https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/)
- Using [DevSkim](https://github.com/microsoft/devskim) IDE extensions/language analyzers

#### Using a memory safe by default language with developer best practices and language processors, post processors etc., but no automated tooling

- Following the [Rustnomicon](https://doc.rust-lang.org/nomicon/intro.html) careful practices when using unsafe blocks in Rust
- Following best practices (LINK NEEDED) when using the Go [unsafe](https://pkg.go.dev/unsafe#pkg-overview) package
- Following [Javascript Memory Management](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management) practices
- Ensuring [soundness](https://rust-lang.github.io/unsafe-code-guidelines/glossary.html#soundness-of-code--of-a-library) of unsafe Rust code

#### Using a memory safe by default language without developer best practices

- Using unsafe blocks in Rust [without assessing the entire module in which the unsafe code appears](https://github.com/ossf/Memory-Safety/issues/15#issuecomment-1847939439)
- Using the [no_mangle](https://github.com/rust-lang/rust/issues/28179) attribute in Rust
- Using compiler options which turn off some or all of the compiler's memory safety checks
- Disabling .NET's source code [Analyzers](https://learn.microsoft.com/en-gb/dotnet/fundamentals/code-analysis/overview?tabs=net-8) during build

#### Using a non-memory safe by default language with developer best practices and automated tooling to check for memory safety in your code as well as in all your dependencies' code

TO DO

#### Using a non-memory safe by default language with developer best practices and automated tooling to check for memory safety in your code

- [Using compiler options for hardening C and C++ Code](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++.html)
- Using a fuzzer such as [syzkaller](https://github.com/google/syzkaller)
- Using [sanitizers](https://github.com/google/sanitizers)
- Using tools to [detect dangling pointers](https://chromium.googlesource.com/chromium/src/+/HEAD/docs/dangling_ptr.md)
- If using Visual Studio, using the [C/C++ code analysis tool](https://learn.microsoft.com/en-us/cpp/code-quality/code-analysis-for-c-cpp-overview?view=msvc-170)
- If using Visual Studio, using the [C++ Core Guidelines checkers](https://learn.microsoft.com/en-us/cpp/code-quality/using-the-cpp-core-guidelines-checkers?view=msvc-170)
- Using [CodeQL](https://codeql.github.com/) for the [languages that CodeQL supports](https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/)
- Using [BinSkim](https://github.com/microsoft/binskim) to analyze binaries
- Using [DevSkim](https://github.com/microsoft/devskim) IDE extensions/language analyzers

#### Using a non-memory safe by default language with developer best practices, but no automated tooling

- [Using attributes such as `cleanup` and classes when writing C](https://lwn.net/Articles/934679/) (and depending on developers to manually check this)
- Following the [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines) when writing C++
- Using the [C++ Compiler Hardening Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides) when compiling C++ code
- Isolating code that processes un-trusted data from code that performs direct memory management operations or uses raw pointers (see [Language-theoretic Security](https://github.com/ossf/Memory-Safety/pull/20))
- Using [smart pointers](https://learn.microsoft.com/en-us/cpp/cpp/smart-pointers-modern-cpp?view=msvc-170)

#### Using a non-memory safe by default language without developer best practies or automated tooling

Using raw C or C++ (or old versions of C and C++ language and compiler)

## The Continuum - Getting to a Better State with re: to memory safety

TO DO

## FAQ

### Is there a way to be COMPLETELY memory safe?

In theory, yes. In reality...it's very hard. It is theoretically possible to write C++ code in a way that is free from memory safety bugs. In practice, however, we still see a very large number of memory safety related security vulnerabilities every year - known vulnerabilities that could be prevented if the code were written in a memory safe by default language.

This is not to say that using a memory safe by default language will protect you from all vulnerabilities. Saying something is "default" also implies that there are ways of using the language in a non default way. This is also true of your software's dependencies - for example, your Rust code may be free of unsafe blocks (or, at least, use them sparingly), but an Open Source package you depend on may not be. Evaluating the safety of your software includes evaluating anything your software depends on.

It is also possible that your software written in a memory safe by default language will need to interface with software written in a non-memory safe by default language (for example, Rust code which must interface with a C++ driver).

No matter where your software is on this memory safety continuum, you will still need to exercise some level of personal/professional judgement on what is an acceptable amount of risk and what is not.

### Are you saying we should just re-write billions of lines of C and C++ code in Rust?

No.

This is not a real world possibility. Even if it were, it would not be practical nor would it be truly helpful.

There are times a rewrite of a particular section of software (such as one where vulnerabilities are particularly prevalent) may be necessary. However, this SIG's focus is not on rewriting the world in Rust (or any other language). Instead, it is on helping developers (and others) understand the memory safety of their code now and how to improve it in meaningful and achievable ways.

### Why do you rank using automated tooling higher than just using developer best practices?

The amount software that has already been produced is staggering - and it is only growing every day. Expecting every developer to manually check their code (and the code their code interacts with) is no longer practical or possible. Automated tooling must be used to catch (at the least) known, common vulnerabilities that a developer may unintentionally introduce in their code.
