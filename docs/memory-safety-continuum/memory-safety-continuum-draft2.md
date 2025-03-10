# The Memory Safety Continuum

## Introduction

Much of the conversation around software memory safety has treated the concept as if it were a binary where software is either memory safe or it is not. The truth, as is often the case, is more complex. In an ideal world, we would all write our software in memory safe by default languages, never needing to use an unsafe block or to interface with software written in a non-memory safe by default language. We do not live in that world, however, and are unlikely to live in that world any time soon. Memory safety in software should be considered a continuum, rather than being binary. Within a continuum, even if we are never at the ideal, we can strive to improve with every line of code we write - whether it is net new code, changes to code we are responsible for maintaining or (when appropriate) targeted rewrites of existing code.

In the document, we present the idea of the memory safety continuum - defining various stages and helping you understand where on the continuum the software you write falls today. It is important to understand that different stages may apply to different areas of the same code base. Even if you write the majority of your software in a language like Rust, you will likely still need to interface with existing code written in C or C++, and these interfaces will require different practices for memory safety than other areas of your code base. The primary audience for this document is developers who want to write safer code. It will also likely provide value to engineering managers, product managers, project managers, and anyone else who wants to better understand memory safety in software.

Becoming more memory safe is a iterative process, no matter where you start on the continuum. This is especially true when dealing with large existing codebases. Small steps, such as introducing memory safe abstractions over non-memory safe code, can make a big difference over time.

### Definitions

The OpenSSF Memory Safety SIG was created with the mission of understanding and reducing memory safety vulnerabilities in Open Source Software. One of our first tasks was to define memory safety for the purpose of our group's work. We considered definitions from various sources and, ultimately, came to a consensus on **[this definition](https://github.com/ossf/Memory-Safety/blob/main/docs/definitions.md)**. While Wikipedia may not traditionally be considered a good source to cite, the crowd editors of [the Memory safety entry](https://en.wikipedia.org/wiki/Memory_safety) have produced a comprehensive classification list of memory safety errors. Memory safety errors are the class of error that memory safe by default languages seek to eliminate.

We also came to a consensus on using the terms "memory safe by default" for languages such as Rust, Go, and C# and "non-memory safe by default" for languages such as C and C++.

## The Continuum

This continuum, ordered from "most safe" to "least safe", is intended to help you define and understand the memory safety of your software and what you can do to improve it. We propose that developers and organizations should use modern toolchains and follow current best practices for their software ecosystems. In particular, whenever there is a memory safe feature or workflow, it should be adopted over a non-memory safe variant.

### 1. Writing software in Memory Safe By Default Languages

Whenever possible/practical, you should use a memory safe by default language (such as Rust, Go, Python, Java, JavaScript, C#) when writing new software. Having memory safety incorporated directly into the language forces good safety practices at compile time as the code is being written. Developers get real time feedback as they create and compile their code. It is certainly possible and sometimes necessary to bypass some of the compiler's safety checks through the use of unsafe blocks and functions. However, memory safe by default languages force developers to intentionally choose unsafety (and, even when they do, to only use unsafety in contained and limited areas of the code), while non-memory safe by default languages depend on developers to intentionally (and continually) choose safety. If it is possible to escape into unsafe blocks, it is natural to ask whether developers will default to using them, negating the advantage of using a memory safe by default language. In 2022, as Google scaled up its use of Rust within the Android Open Source Project, they noted "In general, use of unsafe in Android’s Rust appears to be working as intended. It’s used rarely, and when it is used, it’s encapsulating behavior that’s easier to reason about and review for safety" [^1].

Even when a language is memory safe by default, it is still vital to follow that language ecosystem's best practices and to use external tools to ensure safety not only within your code, but also within dependencies that your code pulls in. Nearly all Open Source software (and likely most close source software) depends on external libraries and packages to function. Care also needs to be exercised to check your dependencies for vulnerabilities.

There are several ways to enhance the safety of your and your dependencies' code. We have captured these enhancements in these substages of this section of the continuum, ordered from most to least ideal.

* 1.1: Using developer best practices and automated tooling to verify safety in both your and your dependencies' code ([Examples](#memory-safe-by-default-language-automated-tooling-to-provide-additional-checks-to-your-dependencies))
* 1.2: Using developer best practices and automated tooling to verify safety *only* in your code ([Examples](#memory-safe-by-default-language-automated-tooling-to-provide-additional-checks-to-your-code))
* 1.3: Using developer best practices *only* ([Examples](#memory-safe-by-default-language-ecosystem-best-practices))

[^1]: [Memory Safe Languages in Android 13](https://security.googleblog.com/2022/12/memory-safe-languages-in-android-13.html)

### 2. Using Memory Safe by Default Languages to interface with Non-Memory Safe By Default Languages

While new software is increasingly being written in memory safe by default languages, there are billions of existing lines of code written in non-memory safe by default languages. Targeted rewrites of highly used, highly vulnerable software components may be necessary and beneficial to the safety of the Open Source ecosystem, but we do not advocate for mass rewrites of all existing code written in non-memory safe by default languages.

It is and will continue to be necessary for software written in memory safe by default languages to interact with software written in non-memory safe by default languages through foreign function interfaces (FFI). FFI is one of the primary uses for unsafe blocks within Rust (as well as within other languages).

There are some general best practices for interfacing between memory safe by default and non-memory-safe by default languages, as well as language-ecoystem specific practices. We have captured these enhancements in the following substages.

* 2.1: Using general and language ecosystem specific best practices for safely interfacing between memory safe by default and non-memory safe by default languages ([Examples](#language-specific-best-practices))
* 2.2: Using general best practices for safely interfacing between memory safe by default and non-memory-safe by default languages ([Examples](#general-interfacing-best-practices))

We expect further developments in this space and will update this continuum as they emerge.

### 3. Using Non-Memory Safe By Default Languages

While we do advocate for writing new code in memory safe by default languages, we recognize this is not always possible or practical. Existing software must be maintained and often expanded, regardless of what language it is written in.

There are several ways to enhance the safety of your and your dependencies' code when written in a non-memory safe by default language. These principles ended up being the same as with memory safe by default languages, though applied a little differently. While there are advantages and disadvantages to various language ecosystems, the principles of solid software engineering remain consistent. We have captured these enhancements in these substages of this section of the continuum, ordered from most to least ideal.

* 3.1: Using developer best practices and automated tooling to verify safety in both your and your dependencies' code ([Examples](#non-memory-safe-by-default-language-automated-tooling-to-provide-additional-checks-to-your-dependencies))
* 3.2: Using developer best practices and automated tooling to verify safety *only* in your code ([Examples](#non-memory-safe-by-default-language-automated-tooling-to-provide-additional-checks-to-your-code))
* 3.3: Using developer best practices *only* ([Examples](#non-memory-safe-by-default-language-ecosystem-best-practices))

## Conclusion

Wherever you, your company, your developers, and your products are on the memory safety continuum, there are languages, tools, and best practices that you can and should deploy to enhance the memory safety of your product and development methodology.

## FAQs

### Is there a way to be COMPLETELY memory safe?

In theory, yes. In reality...it's very hard. It is theoretically possible to write C++ code in a way that is free from memory safety bugs. In practice, however, we still see a very large number of memory safety related security vulnerabilities every year - known vulnerabilities that could be prevented if the code were written in a memory safe by default language (as noted by Microsoft[^2], Google[^3], and the US National Security Agency[^4]).

This is not to say that using a memory safe by default language will protect you from all vulnerabilities. Saying something is "default" also implies that there are ways of using the language in a non default way. This is also true of your software's dependencies - for example, your Rust code may be free of unsafe blocks (or, at least, use them sparingly), but an Open Source package you depend on may not be. Evaluating the safety of your software includes evaluating anything your software depends on.

It is also possible that your software written in a memory safe by default language will need to interface with software written in a non-memory safe by default language (for example, Rust code which must interface with a C++ driver).

No matter where your software is on this memory safety continuum, you will still need to exercise some level of personal/professional judgement on what is an acceptable amount of risk and what is not.

[^2]: [A proactive approach to more secure code](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/)
[^3]: [The More You Know, The More You Don't Know](https://googleprojectzero.blogspot.com/2022/04/the-more-you-know-more-you-know-you.html)
[^4]: [Software Memory Safety](https://media.defense.gov/2022/Nov/10/2003112742/-1/-1/0/CSI_SOFTWARE_MEMORY_SAFETY.PDF)

### Are you saying we should just re-write billions of lines of C and C++ code in Rust?

No.

This is not a real world possibility. Even if it were, it would not be practical nor would it be truly helpful.

There are times a rewrite of a particular section of software (such as one where vulnerabilities are particularly prevalent) may be necessary. However, our focus is not on rewriting the world in Rust (or any other language). Instead, it is on helping developers (and others) understand the memory safety of their code now and how to improve it in meaningful and achievable ways.

### Why do you rank using automated tooling higher than just using developer best practices?

The amount software that has already been produced is staggering - and it is only growing every day. Expecting every developer to manually check their code (and the code their code interacts with) is no longer practical or possible. Automated tooling must be used to catch (at the least) known, common vulnerabilities that a developer may unintentionally introduce in their code.

## Examples

### 1. Writing software in Memory Safe By Default Languages

#### Memory safe by default language ecosystem best practices

* Following the [Rustnomicon](https://doc.rust-lang.org/nomicon/intro.html) careful practices when using unsafe blocks in Rust
* Following best practices (LINK NEEDED) when using the Go [unsafe](https://pkg.go.dev/unsafe#pkg-overview) package
* Following [Javascript Memory Management](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management) practices
* Ensuring [soundness](https://rust-lang.github.io/unsafe-code-guidelines/glossary.html#soundness-of-code--of-a-library) of unsafe Rust code
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-memory-safe-by-default-languages.md)

#### Memory safe by default language automated tooling to provide additional checks to your code

* Using the [Go Data Race Detector](https://go.dev/doc/articles/race_detector)
* Using other tools such as [govulncheck, fuzzing, and vet](https://go.dev/doc/security/best-practices) when writing Go code
* Using a mutation tester such as [cargo-mutants](https://github.com/sourcefrog/cargo-mutants)
* Using [CodeQL](https://codeql.github.com/) for the [languages that CodeQL supports](https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/)
* Using [DevSkim](https://github.com/microsoft/devskim) IDE extensions/language analyzers
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-memory-safe-by-default-languages.md)

#### Memory safe by default language automated tooling to provide additional checks to your dependencies

* Using a fuzzer such as [AFL++](https://github.com/AFLplusplus/AFLplusplus) on both your own code and third party code

### 2. Using Memory Safe by Default Languages to interface with Non-Memory Safe By Default Languages

#### General interfacing best practices

* Separating all FFIs into a separate crate/module/package so that it can be audited in isolation. All exported symbols from that crate/module/package should be memory safe. [Source](https://github.com/ossf/Memory-Safety/issues/36#issuecomment-2477083785)
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-interfacing.md)

#### Language specific best practices

* Using the [bindgen](https://crates.io/crates/bindgen) crate
* Using the [cbindgen](https://crates.io/crates/cbindgen) crate
* Using the [cxx](https://crates.io/crates/cbindgen) crate
* Avoiding using the legacy Java Native Interface (JNI) APIs. If needed, prefer the newer Foreign Function & Memory (FFM) APIs introduced in Java 22.
* Monitoring or preventing JNI API occurrences (e.g. uses of the `native` keyword or calls to `System.load()` or `System.loadLibrary()`) in your code using [static code analysis tools](https://www.baeldung.com/tag/static-analysis).
* If using JNI is your only option, following all the same best practices as you would with a [non memory-safe language](best-practice-non-memory-safe-by-default-languages.md).
* Always enabling the [-Xcheck:jni JVM option](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/clopts002.html#CHDHCBBG) to activate additional validation of JNI functions' arguments. Even if your code does not use JNI, your third-party dependencies might (JDBC drivers are a common example).
* Using the [-verbose:jni JVM option](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/clopts002.html#CHDCHGEE) can also be useful to detect or troubleshoot JNI issues but beware of the potential performance as it could cause a lot of extra log messages if JNI is heavily used in your application.
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-interfacing.md)


### 3. Using Non-Memory Safe By Default Languages

#### Non-memory safe by default language ecosystem best practices

* [Using attributes such as `cleanup` and classes when writing C](https://lwn.net/Articles/934679/) (and depending on developers to manually check this)
* Following the [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines) when writing C++
* Using the [C++ Compiler Hardening Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides) when compiling C++ code
* Isolating code that processes un-trusted data from code that performs direct memory management operations or uses raw pointers (see [Language-theoretic Security](https://github.com/ossf/Memory-Safety/pull/20))
* Using [smart pointers](https://learn.microsoft.com/en-us/cpp/cpp/smart-pointers-modern-cpp?view=msvc-170)
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-non-memory-safe-by-default-languages.md)

#### Non-memory safe by default language automated tooling to provide additional checks to your code

* [Using compiler options for hardening C and C++ Code](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++.html)
* Using a fuzzer such as [syzkaller](https://github.com/google/syzkaller)
* Using [sanitizers](https://github.com/google/sanitizers)
* Using tools to [detect dangling pointers](https://chromium.googlesource.com/chromium/src/+/HEAD/docs/dangling_ptr.md)
* If using Visual Studio, using the [C/C++ code analysis tool](https://learn.microsoft.com/en-us/cpp/code-quality/code-analysis-for-c-cpp-overview?view=msvc-170)
* If using Visual Studio, using the [C++ Core Guidelines checkers](https://learn.microsoft.com/en-us/cpp/code-quality/using-the-cpp-core-guidelines-checkers?view=msvc-170)
* Using [CodeQL](https://codeql.github.com/) for the [languages that CodeQL supports](https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/)
* Using [BinSkim](https://github.com/microsoft/binskim) to analyze binaries
* Using [DevSkim](https://github.com/microsoft/devskim) IDE extensions/language analyzers
* [More best practices](https://github.com/ossf/Memory-Safety/blob/main/docs/best-practice-non-memory-safe-by-default-languages.md)

#### Non-memory safe by default language automated tooling to provide additional checks to your dependencies

TO DO
