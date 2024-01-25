# Revised Stream 4 Language

This is a draft of revised language for Stream 4 - Memory Safety of the [Open Source Software Security Mobilization Plan](https://openssf.org/oss-security-mobilization-plan/).

In this doc we have standardized on this terminology/spelling:

* memory safety
* memory-safe
* NOT memory-safely
* NOT unsafety

## The Problem

It is common for vulnerabilities to result from a program mismanaging memory. These types of vulnerabilities are called memory safety vulnerabilities.

Some programming languages, including Rust, Go, JavaScript, and Java, are commonly referred to as "memory-safe languages". By default, these languages prevent programmers from making the mistakes that result in classes of memory safety vulnerabilities. Other languages, including C and C++, are commonly referred to as "memory unsafe languages". Be default, these languages do not prevent programmers from making the mistakes that result in classes of memory safety vulnerabilities.

Microsoft estimates that 70% of the vulnerabilities in its products (those that were built with memory unsafe languages) over the past decade are memory safety vulnerabilities[^1]. Google estimates that 90% of vulnerabilities in Android media and Bluetooth components are memory safety vulnerabilities[^2].

A 2021 Google Project Zero analysis of vulnerabilities that were detected and disclosed as being exploited in the wild found that 67% of vulnerabilities (in software written in memory-unsafe by default languages) were due to a lack of default memory safety. “Memory corruption vulnerabilities have been the standard for attacking software for the last few decades and it’s still how attackers are having success”, they stated[^3].

In their information sheet on Software Memory Safety, the National Security Agency states "Malicious cyber actors can exploit these vulnerabilities for remote code execution or other adverse effects, which can often compromise a device and be the first step in large-scale network intrusions"[^4].

[^1]: https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/
[^2]: https://security.googleblog.com/2019/05/queue-hardening-enhancements.html
[^3]: https://googleprojectzero.blogspot.com/2022/04/the-more-you-know-more-you-know-you.html
[^4]: https://media.defense.gov/2022/Nov/10/2003112742/-1/-1/0/CSI_SOFTWARE_MEMORY_SAFETY.PDF

## Our Proposed Approach

Unlike many other types of vulnerabilities, we know how to massively reduce (if not outright remove) complete classes of memory safety vulnerabilities. Whenever possible or practical, software should be written in or moved to programming languages which, in their default settings, prevent memory safety vulnerabilities.

For existing code  bases that are not able to move away from memory-unsafe by default languages, there are tools and specifications which can reduce memory safety vulnerabilities. These tools and specifications should continue to be developed. Software that cannot be moved to a memory-safe by default language should use these tools and move to these specifications.

The work we plan to do to reduce the number of memory safety vulnerabilities consists of five parts.

1. Wherever possible, move the internet’s most critical software to memory-safe by default languages with an efficient strategy that emphasizes upgrading the most security-sensitive components first.
2. Invest in the tools that allow systems engineers to move lower-level systems-level code to a memory-safe by default language. This will allow us to have impact beyond just the most critical projects. We will focus on tools for systems-level code because it is the most ubiquitous and vulnerable software in the ecosystem, and it is the most likely to be written in memory-unsafe by default languages.
3. Invest in tools/specifications that improve memory safety when a migration to a memory-safe by default language is not possible [^5].
4. Invest in educating software engineers at all levels about the importance of memory safety and that skills for reliably and securely engineering computer software are critical

[^5]: https://github.com/isocpp/CppCoreGuidelines

### Moving critical software infrastructure to memory-safe by default languages

This component of our strategy will rely on [Prossimo](https://www.memorysafety.org/), a project run by the nonprofit [Internet Security Research Group (ISRG)](https://www.abetterinternet.org/). The Prossimo project works to identify the most critical software infrastructure that needs to be moved to a memory-safe by default language, plan effective and efficient migrations with stakeholders, and oversee execution of the plans.

The top-level risk criteria that Prossimo uses to identify potential investments is:

1. Very widely used (nearly every server and/or client)
2. On a network boundary
3. Performing a critical function
4. Written in languages that do not provide memory safety by default (e.g. C, C++)

Of software that fits those criteria, the following opportunity criteria are evaluated:

1. Is this a library or component that can be used in many different projects?
2. Can we efficiently replace key components with existing memory-safe libraries?
3. Are funders willing to fund the work?
4. Are the maintainers on board and cooperative?

Based on all of the above criteria, there are Prossimo initiatives underway for the Linux kernel and applications and libraries related to Transport Layer Security (TLS), Domain Name System (DNS), and Network Time Protocol (NTP).

### Investing in Safer Systems Development Tools

Much of the world’s most ubiquitous and critical software is lower-level systems software that underlies almost every computing device in the world (e.g. kernels, basic networking functionality, timekeeping). It’s in banks, hospitals, and government systems. This software is typically written in a memory-unsafe by default language called C, because for much of computing history C was the go-to language for systems software development.

Because lower-level software has more operational constraints than higher-level software (e.g. it typically cannot tolerate a runtime or memory management via garbage collection), developing a memory-safe language suitable for systems software is particularly challenging. The Rust language has met that challenge, however, and is an excellent candidate for replacing C in many systems applications.

We plan to invest in the tools that allow systems engineers to move their software to Rust. This means investing in improving package management, compilers, and Foreign Function Interface (FFI) generators. In many cases this will include providing interfaces compatible with existing widely-used components to enable transition. With these tools, adoption of a memory-safe by default alternative will scale much faster without replication of efforts. We also propose to invest in similar efforts in the Go and Java communities. Both languages are frequently used for systems-level and network applications, including in security-sensitive environments. We propose to reach out to the community through a series of grant-making efforts focused on the same priorities and criteria described above, initially targeting  existing projects that need an extra push to get to a production release and adoption and those that may help other workstreams in this plan. These investments will be made primarily via ISRG, the Rust Foundation for Rust-related work, the Eclipse Foundation for Java-related work, and independent grants for Go-related work.

### Invest in tools and specifications that improve memory safety when migration is not possible

When movement to a memory-safe by default language is not possible, we will invest in tools that improve memory safety in C and C++ code bases - including specifications and automated tools.

TO DO - need examples.

### Invest in Education

It is important to not only provide tooling for developers to develop software with memory safety, but sharing HOW and WHY to do so is equally of value.  There are several areas where educational materials, training, and job aids should be identified or created to help developers quickly learn about memory safe languages, how to use more memory-safe coding techniques in older languages, as well as the threats and vulnerabilities non-memory-safe coding practices can incur.  We propose to create a reference library and educational materials on:

* the threats and vulnerabilities that exist around memory safety coding flaws
* the benefits of developing using memory safe languages
* references to authoritative guides for memory-safe languages
* educational training material for older languages, such as C and C++, on how to develop using memory-safety techniques and safe memory handling practices
* spread awareness and help others develop skills in memory safe languages and secure coding techniques through blogs, podcasts, conference presentations, and training classes

### Challenges

#### Dependency Chains

Many memory safe by default languages (e.g. Rust, Go, Python) have relatively advanced package management models, including more advanced dependency management tools. This leads to dependency chains that are typically significantly larger than those of equivalent C programs.

Longer dependency chains are not necessarily specific to memory safe languages. However, since many of the most important memory safe languages have larger dependency chains, dealing with larger chains is a major issue for the adoption of memory safe languages.

If memory safe programs are to gain more widespread adoption, particularly as components of operating systems, we will need to address both the logistical and web-of-trust challenges presented by longer dependency chains. This could involve trying to shorten chains and/or gaining confidence in how we manage longer chains.
