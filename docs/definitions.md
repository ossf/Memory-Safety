# Useful Definitions

The document contains some useful definitions used in this group's work.

## Memory Safe by Default

[Based off the definition in wikipedia](https://en.wikipedia.org/wiki/Memory_safety).

A memory safe by default language prevents (by default) common memory safety vulnerabilities, including:

**Access errors (invalid read/write of a pointer)**

* Buffer overflow
* Buffer over-read
* Invalid page fault
* Use after free[^1]

**Uninitialized variables (variable that has not been assigned a value is used)**

* Null pointer deference
* Wild pointers
* Uninitialized variables being used

**Memory leak (memory usage is not tracked or is tracked incorrectly)**

* Stack exhaustion
* Heap exhaustion
* Double free
* Invalid free
* Mismatched free
* Unwanted aliasing

A memory safe by default language also addresses the following:

**Race Conditions**

* Concurrent read/writes to shared memory

Some memory safe by default languages prevent data races (such as Rust), but others (such as Java, Go, and C#) require the use of additional conventions, packages, or libraries to prevent data races. Please see [Best Practices for Memory Safe by Default Languages](best-practice-memory-safe-by-default-languages.md)

## Undefined Behavior

[From the definition in the Stack Overflow Wiki](https://stackoverflow.com/tags/undefined-behavior/info).

"In computer programming, undefined behavior (informally "UB") refers to computer code whose behavior is not specified by the programming language standard under certain conditions.

The standards for some languages, most notably C and C++, leave certain aspects undefined, meaning the standard imposes no requirements whatsoever on the outcome. Implementations may regard such actions as erroneous, diagnosing them or not as they see fit, or may specify that they behave in some possibly-useful fashion without regard for whether the Standard requires them to do so."

[^1]: This definition refers to a use after free error with regard to memory allocation and pointers. However, in this SIG's discusssions, we also realized there is a different kind of use after free error that can occur due to the improper sharing of heap objects where objects may be accessed on the heap level after they are freed on the object level. These errors are also relevant to memory safety. Please see [this GitHub issue](https://github.com/ossf/Memory-Safety/issues/29) for more discussion.
