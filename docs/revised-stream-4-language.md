# Revised Stream 4 Language

This is a draft of revised language for Stream 4 - Memory Safety of the [Open Source Software Security Mobilization Plan](https://openssf.org/oss-security-mobilization-plan/).

## The Problem:

It is common for vulnerabilities to result from a program mismanaging memory. These types of vulnerabilities are called memory safety vulnerabilities. 

Some programming languages, including Rust, Go, and Java, are commonly referred to as "memory safe languages". By default, these languages prevent programmers from making the mistakes that result in classes of memory safety vulnerabilities. Other languages, including C and C++, are commonly referred to as "memory unsafe languages". Be default, these languages do not prevent programmers from making the mistakes that result in classes of memory safety vulnerabilities.

Microsoft estimates that 70% of the vulnerabilities in its products (those that were built with memory unsafe languages) over the past decade are memory safety vulnerabilities[^1]. Google estimates that 90% of vulnerabilities in Android media and Bluetooth components are memory safety vulnerabilities[^2]. 

A 2021 Google Project Zero analysis of vulnerabilities that were detected and disclosed as being exploited in the wild found that 67% of vulnerabilities (in software written in memory unsafe languages) were due to a lack of default memory safety. “Memory corruption vulnerabilities have been the standard for attacking software for the last few decades and it’s still how attackers are having success”, they stated[^3].

In their information sheet on Software Memory Safety, the National Security Agency states "Malicious cyber actors can exploit these vulnerabilities for remote code execution or other adverse effects, which can often compromise a device and be the first step in large-scale network intrusions"[^4].

[^1]: https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/
[^2]: https://security.googleblog.com/2019/05/queue-hardening-enhancements.html
[^3]: https://googleprojectzero.blogspot.com/2022/04/the-more-you-know-more-you-know-you.html
[^4]: https://media.defense.gov/2022/Nov/10/2003112742/-1/-1/0/CSI_SOFTWARE_MEMORY_SAFETY.PDF

## Our Proposed Approach

Unlike many other types of vulnerabilities, we know how to massively reduce (if not outright remove) complete classes of memory safety vulnerabilities. Whenever possible or practical, software should be written in or moved to programming languages which, in their default settings, prevent memory safety vulnerabilities.

For existing code  bases that are not able to move away from memory unsafe by default languages, there are tools and specifications which can reduce memory safety vulnerabilities. These tools and specifications should continue to be developed. Software that cannot be moved to a memory safe by default language should use these tools and move to these specifications.

The work we plan to do to reduce the number of memory safety vulnerabilities consists of five parts.

1. Wherever possible, move the internet’s most critical software to memory safe by default languages with an efficient strategy that emphasizes upgrading the most security-sensitive components first.
2. When it is not possible/practical to move critical software to a memory safe by default language, move the software to a language specification which reduces memory safety vulnerabilities and use tools to enforce the specification's rules[^1].
3. Invest in the tools that allow systems engineers to move lower-level systems-level code to a memory safe by default language. This will allow us to have impact beyond just the most critical projects. We will focus on tools for systems-level code because it is the most ubiquitous and vulnerable software in the ecosystem, and it is the most likely to be written in memory unsafe by default languages.
4. Invest in tools/specifications that improve memory safety when a migration to a memory safe by default language is not possible. 
5. Invest in educating software engineers at all levels about the importance of memory safety and that skills for reliably and securely engineering computer software are critical 

[^1]: https://github.com/isocpp/CppCoreGuidelines

