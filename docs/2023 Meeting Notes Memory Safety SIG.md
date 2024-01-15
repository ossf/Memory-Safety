
<h2>Memory Safety SIG</h2>


<h3>Antitrust Policy Notice</h3>


Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in, any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws. Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

<h3>Code of Conduct</h3>


All OpenSSF Meetings must comply with the Code of Conduct: [https://openssf.org/community/code-of-conduct/](https://openssf.org/community/code-of-conduct/)

This group is part of the OpenSSF Best Practices WG.

Please use the 2024 Meeting Notes below:

[2024 Meeting Notes](https://docs.google.com/document/d/1RnIzqeKyrOJvs6vQ8xGH6TjZDoEFaGUs1NkAx--v_3Y/edit?usp=sharing)


<h2>2023-12-14</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>Microsoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Andrew Fryer
   </td>
   <td>
   </td>
   <td>he/him
   </td>
  </tr>
</table>


<h2>Agenda</h2>




* Welcome new friends
* Help Scribe
* Canceling next meeting (scheduled for Dec 28) for holidays
* Add JS as example of memory safe by default language https://github.com/ossf/Memory-Safety/pull/17
* Revised draft criteria for evaluating OSS memory safety initiatives/projects [https://github.com/ossf/Memory-Safety/pull/16](https://github.com/ossf/Memory-Safety/pull/16)
* Initial content for safety practices in memory safe by default languages [https://github.com/ossf/Memory-Safety/pull/18](https://github.com/ossf/Memory-Safety/pull/18)
* Discuss Creating a Memory Safety W3C-style workshop (Avishay)
    * Thinking of idea:
        * Memory safety when rewrite is not feasible
        * Stories from well established organizations move to rust
        * OS level memory safety
        * Memory unsafety in memory-safe-by-deault languages (python, rust, go)
        * Use the next meeting to suggest who can help lead this
* Scorecard checks for memory safety. 
    * We can leverage content such as the binary hardening guide or the Best Practices - Memory-Safe By Default Languages for adding memory-safety checks to Scorecard.
    * Agreed to open an issue on the SC repo once the PR for Best Practices - Memory-Safe By Default Languages is merged (Avishay and Nell)

<h2>2023-11-30</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Andrew Fryer
   </td>
   <td>
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Brian Crooks
   </td>
   <td>Datalytica
   </td>
   <td>he/him
   </td>
  </tr>
</table>


<h2>Agenda</h2>




* Welcome new friends
    * Welcome to Ryan Ware (Intel) who leads the security tooling WG.
* Help Scribe
* Revised draft criteria for evaluating OSS memory safety initiatives/projects https://github.com/ossf/Memory-Safety/pull/16
*  Practice evaluating a project according to the draft guidelines (not doing an actual evaluation, just practice)
    * [https://www.memorysafety.org/initiative/rustls/](https://www.memorysafety.org/initiative/rustls/)
        * definitely qualifies for funding
    * [https://github.com/BurntSushi/ripgrep](https://github.com/BurntSushi/ripgrep)
        * we would have to discuss with the author
*  Update on binary hardening guides for other languages https://github.com/ossf/Memory-Safety/issues/15

<h2>2023-11-16</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>Microsoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Charles C Palmer
   </td>
   <td>IBM Research; Dartmouth
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Seth Larson
   </td>
   <td>PSF
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Michael Droettboom
   </td>
   <td>Microsoft; Python
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Andrew Fryer
   </td>
   <td>
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
    * Welcome to Ryan Ware (Intel) who leads the security tooling WG.
* Help Scribe
* Identifying/Evaluating Memory Safety Efforts
    * [https://github.com/ossf/Memory-Safety/pull/13](https://github.com/ossf/Memory-Safety/pull/13)
        * Does this meet our definition of memory safety?
        * Criticality?
        * Severity?
            * E.g., libwebp
* Memory Safety in other languages
    * (C/C++ has [https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides))
    * Java
        * [Panama](https://openjdk.org/projects/panama/)
    * Python
        * Is the CPython runtime under the charter of this community?
        * RFI: [https://www.regulations.gov/comment/ONCD-2023-0002-0107](https://www.regulations.gov/comment/ONCD-2023-0002-0107)
        * C/C++ is still dominant for writing FFIs/binary extensions for Python, but Rust is growing.
        * Would be good to have a guide on using Python flags that improve safety.
        * Perhaps we could collaborate with [Anaconda](https://anaconda.org) or [NumFocus](https://numfocus.org).
    * .NET
    * Etc.
* Future Work
    * Try compiling the CPython runtime with security flags and see if it passes the test suite

<h2>2023-11-02</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>Microsoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Ryan Ware
   </td>
   <td>Intel
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Jay White
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
    * Welcome to Ryan Ware (Intel) who leads the security tooling WG.
* Help Scribe
* Definition of Memory Safety PR (Check for new one at time of meeting)
    * [https://github.com/ossf/Memory-Safety/pull/12](https://github.com/ossf/Memory-Safety/pull/12)
    * Review and merge the PR during the call
    * 
* Funding/Project Support Program Criteria PR 
    * [https://github.com/ossf/Memory-Safety/pull/13](https://github.com/ossf/Memory-Safety/pull/13)	
    * Question in the call regarding if this change should be at the SIG level, at the WG level, or at the foundation level. Added as a remark to the PR.
    * We agree to let CRob review the PR.
* Hardening Guides for more languages
    * Following the [C/C++ binary hardening guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Compiler-Hardening-Guides) by the BEST WG, we’re investigating if other languages should be added to the guide.
    * Investigate compilers of different languages, can they be compiled unsafely.
    * A proposal to initiate a spike investigating if other languages can be complied in a memory unsafe manner
        * Nell: Rust, Go
        * Avishay: Python, Java, .Net, and open an issue in the repo
* Ossf response to the ONCD RFP (link?) (Ryan Ware)
    * 
    * 

<h2>2023-10-05</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Gabriel Dos Reis
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><em>X</em>
   </td>
   <td>Charles C Palmer
   </td>
   <td>IBM Research; Dartmouth
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe
* Definition of Memory Safety
    * PR: https://github.com/ossf/Memory-Safety/pull/12
* Wikipedia has the clearest definition so far.  Looking for better definition.  Or use “derived from”.
* “Race condition” -> “memory race condition”
* GDR to prepare an amendment to the PR
* Undefined Behavior: we have definition from C and C++ standards; we don’t have a standard yet for Rust, but we could link to its in-progress reference.
* CHERI: [https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/](https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/)
* [The Urgent Need for Memory Safety in Software Products | CISA](https://www.cisa.gov/news-events/news/urgent-need-memory-safety-software-products)
* Microsoft Project Verona: [https://microsoft.github.io/verona](https://microsoft.github.io/verona)
* Capabilities-based addressing (used in IBM System/38, IBM AS/400, IBM i, Intel APX, ARM CHERI): [https://en.wikipedia.org/wiki/Capability-based_addressing](https://en.wikipedia.org/wiki/Capability-based_addressing)
* [https://saturncloud.io/blog/understanding-and-fixing-pytorch-memory-leak-on-loss-backward-for-gpu-and-cpu/](https://saturncloud.io/blog/understanding-and-fixing-pytorch-memory-leak-on-loss-backward-for-gpu-and-cpu/)
* [https://homes.cs.washington.edu/~levy/capabook/index.html](https://homes.cs.washington.edu/~levy/capabook/index.html)
* [https://dl.acm.org/doi/10.1145/361011.361070](https://dl.acm.org/doi/10.1145/361011.361070)
* PyTorch identified as key project needing attention regarding memory leak.  Does that project belong to this WG’s scope?  Potentially because of funding projects to fix issues?  Needs more clarity.
* Conclusion: Already in scope (needs no special mention); when additional issues are identified then will come back with concerns regarding “code” pipeline. 
* Criteria for recommending an initiative for funding

    Working doc: 

* Attendance happy with the current draft

<h2>2023-09-21</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Gabriel Dos Reis
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe
* Criteria for recommending an initiative for funding

    Working doc: 

* Definition of Memory Safety
    * PR to GitHub repo (Nell)
    * Also add propose definition of undefined behavior (Nell)

Starting point 

(Based on[ this wikipedia article](https://en.wikipedia.org/wiki/Memory_safety))

A memory safe by default language prevents (by default) common memory safety vulnerabilities, including:



* Access errors (invalid read/write of a pointer)
    * Buffer overflow
    * Buffer over-read
    * Race condition
    * Invalid page fault
    * Use after free
* Uninitialized variables (variable that has not been assigned a value is used)
    * Null pointer deference
    * Wild pointers
* Memory leak (memory usage is not tracked or is tracked incorrectly)
    * Stack exhaustion
    * Heap exhaustion
    * Double free
    * Invalid free
    * Mismatched free
    * Unwanted aliasing

<h2>2023-09-05</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>Microsoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>CRob
   </td>
   <td>Intel; TAC
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Sarah Evans
   </td>
   <td>Dell Technologies 
   </td>
   <td>she/her
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe
* Review In progress work
    * [https://github.com/ossf/Memory-Safety/pull/10](https://github.com/ossf/Memory-Safety/pull/10)
    * No objections or conversation. Merged.
* Discuss evaluation criteria for funding initiatives
    * [https://github.com/ossf/Memory-Safety/issues/11](https://github.com/ossf/Memory-Safety/issues/11)
    * There aren’t templates for funding in place yet.
    * Will SIGS recommend funding, and how would we make recommendations
    * How much fundraising in OpenSSF, or seek (transparent) fund pledge from a member.
    * Evaluating memory safety improvements (e.g. 5 vetted projects that improve memory safety) could be helpful to funding conversations by governments. Make “These initiatives have merit” conversations, vs fundraising itself which feels out of scope.
    * How does this conversation relate to Education SIG conversations? Proposal from experts up to the Board for funding based on Mob plan. How things get funded is still unknown, but hopefully will be discussed further at October in person gb meeting. Should discuss projects that request funding (hard cost) vs projects that request resource support (soft cost). Projects that request funding, should have a way to show value for the funding. Think about a decision flow tree. 
    * Do we want projects approaching SIG (tell us about your project and how it improves memory safety), or evaluate projects for technical viability and offer to help (possibly with resources or funding). Projects who are struggling could be pointed to Alpha-Omega if they are a critical project that needs assistance.
    * Request to develop a draft set of criteria for a set of criteria for support. Is it technically viable? Limit scope to “technical viable” at this point? Avishay will work on, and Nell will support.
* Discussion of memory safety RFI
    * [Federal Register :: Request for Information on Open-Source Software Security: Areas of Long-Term Focus and Prioritization](https://www.federalregister.gov/documents/2023/08/10/2023-17239/request-for-information-on-open-source-software-security-areas-of-long-term-focus-and-prioritization) OpenSSF draft response [Response on open source software (OSS) security and memory safe programming languages RFI - Google Docs](https://docs.google.com/document/d/17ZR4GWY77q4NgP73hORvVWQkCj3KRRu-vwqprXIGs2M/edit)
    * Rust not the “one true language”, C++ formally not a memory safe language. Trying to see a balance. Foreign function interface. C bindings (C, Python, Ruby) can use C bindings to call rust libraries if the rust library. This is a viable way to slowly introduce new features or particularly problematic areas.
    * Please put in comments by this weekend.
    * Is there a common definition of memory safety? Tend to use “memory safe by default”, and “memory unsafe by default”. What criteria to be in each. Type safety, buffer overflows, use after freeze. THere are formal definitions, but this SIG isn’t working under a specific one at this time.

<h2>2023-08-10</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>Microsoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Gabriel Dos Reis
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Jay White
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe - Avishay B
* Review In progress work
    * [https://github.com/ossf/Memory-Safety/pull/9](https://github.com/ossf/Memory-Safety/pull/9)
    * PR was reviewed and merged
    * [https://github.com/ossf/Memory-Safety/pull/10](https://github.com/ossf/Memory-Safety/pull/10)
    * Some comments in this PR
        * Linking to the hardening guide
        * Change “switching to memory…” to “using memory …”
        * Discussion raised by GDR about the funding sources
    * [https://github.com/ossf/Memory-Safety/issues/5](https://github.com/ossf/Memory-Safety/issues/5)
        * Best keep this discussion when CRob is on the meeting, since he had some ideas about potential collaboration and workshop this team can work on.
    * [https://github.com/ossf/Memory-Safety/issues/6](https://github.com/ossf/Memory-Safety/issues/6)
    * 
    * 

<h2>2023-07-20</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>CRob
   </td>
   <td>Intel; TAC
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Daniel Frampton
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Charles C Palmer
   </td>
   <td>IBM Research; Dartmouth
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Josh Aas
   </td>
   <td>ISRG
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe - David E
* Review In progress work
    * [https://github.com/ossf/Memory-Safety/pull/8](https://github.com/ossf/Memory-Safety/pull/8)
        * Proposed to merge by Nell.
        * Approved by attendees.
        * CRob will merge.
    * [https://github.com/ossf/Memory-Safety/pull/7](https://github.com/ossf/Memory-Safety/pull/7)
        * Proposed to merge by Nell.
        * Approved by attendees.
        * CRob will merge.
* Proposal to modify meeting cadence by one week
    * Proposal will be sent to mailing list and Slack for feedback from all members.
    * Proposed next meeting July 27.
* CRob - Consider us hosting some type of workshop as a type of “call to action”
    * US Govt CISA asking about progress
    * Virtual or in person?
        * Limited travel budgets at tech companies
    * What outcomes do we want?
    * Converting to memory safe language does not automatically ensure increased safety / security
        * Cost - benefit analysis
        * Memory safety conversion may introduce other security risks
* Has there been any high assurance evaluations in languages like Rust, i.e., FIPS-140 compliance?
    * [https://ferrous-systems.com/ferrocene/](https://ferrous-systems.com/ferrocene/) - Rust in safety critical situations
    * Rust language specification for high assurance

<h2>2023-07-06</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>(regrets)
   </td>
   <td>David A. Wheeler
   </td>
   <td>Linux Foundation
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>MIcrosoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Daniel Frampton
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>David Edelsohn
   </td>
   <td>IBM
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Suraj Gangwar
   </td>
   <td>Freshworks
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe - 
* Review In progress work
    * Discuss PR [https://github.com/ossf/Memory-Safety/pull/8](https://github.com/ossf/Memory-Safety/pull/8) by Josh, regarding large dependency chains of memory safe language.
    * The focus is the trust chain of large dependency. Not so much the logistics of managing dependencies, but more about trusting long chain dependencies.
    * Question from David, why is that inherently different from C? 
        * Dependency trees in typical programs today are different then typical rust programs. One possible cause for this is the ease of modern package managers, vs C package managers that are less dependent on large dependency trees.
        * As an example, mod-TLS has much larger dependency graph than the equivalent C library
        * There’s also a cultural difference in the ecosystems as well as an impedance difference in crates vs libraries.
        * A discussion if that is a rust specific issue:
            * Josh mentions that he same discussion comes up with golang
        * Are we worried about the tools scaling or about maintaining the long dependency chains?
            * The latter, in terms of trust. If we’re packaging 200 crates into the application, that is a large intake.
        * David agrees with Daniel that this is a shared concern for modern application building and packaging.
        * Josh says that this is an attribute of modern languages, not memory safe languages, but nonetheless it is a barrier to memory safe language adoption in the real world right now
    * Nell calls this out as a cultural challenge as well as a technical tooling change that we are trying to fix.
    * The team agreed to continue the discussion over Josh’s PR #8, linked above.
    * Second PR that was discussed is CRob’s education section. Still WIP.
* David W (in absentia): Propose creating a page/document with links to approaches to improvements in memory safety issues in languages (C/C++) where full memory safety isn’t the default. E.g.:
    * Making C++ Memory-Safe Without Borrow Checking, Reference Counting, or Tracing Garbage Collection [https://verdagon.dev/blog/vale-memory-safe-cpp](https://verdagon.dev/blog/vale-memory-safe-cpp) - discussion here: [https://news.ycombinator.com/item?id=36448759](https://news.ycombinator.com/item?id=36448759)
    * Scope-based resource management for the kernel: [https://lwn.net/Articles/934679/](https://lwn.net/Articles/934679/)
    * I’m thinking of starting with a simple Google doc or markdown file to collect this information; it can be spruced up later.
    * Anyone with a large C/C++ code base who wants memory safety will want to look at the options that do *not* require costly rewrites. We may as well provide them with hints about that (and in the long term, a discussion of pros and cons). The challenges involved in using them may convince them that a language switch is needed, but we should help them make informed decisions.
    * We agree to start working on that document!
    * we can start working on that in the memory-safe repo until ready and then contribute it to the guides that are found in the best-practices repo, so that users can find that more easily.
* 

<h2>2023-06-22</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Nell Shamrell-Harrington
   </td>
   <td>Microsoft; Rust Foundation
   </td>
   <td>she/they
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Avishay Balter
   </td>
   <td>MIcrosoft
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>CRob
   </td>
   <td>Intel; TAC
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>x
   </td>
   <td>Jay White
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>y
   </td>
   <td>Charles C Palmer
   </td>
   <td>IBM Research; Dartmouth
   </td>
   <td>he/him
   </td>
  </tr>
  <tr>
   <td>y
   </td>
   <td>Josh Aas
   </td>
   <td>ISRG
   </td>
   <td>he/him
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe - CRob
* Review In progress work
    * [https://github.com/ossf/Memory-Safety/pull/7](https://github.com/ossf/Memory-Safety/pull/7) 
    * Suggested language/tasks around adding Training around Memory Safety
    * Discussion around using “memory-safe”  vs/ “memory safe”
        * Group appears to desire “memory-safe” and “memory safety” and not “memory-safely”
        * @CRob will adjust pr with desired structure @Nell will adjust rest of doc
        * Avashay mentions if we also desire to try and influence college curricula?  Group agrees to also attempt this route as well
    * Gabby will provide suggested wording for examples tools & specs ([Issue 5](https://github.com/ossf/Memory-Safety/issues/5))
    * Josh raises concern - problem with rewriting tools in Rust, challenges getting OSes to ship these alternate languages.  OSes are geared for more traditional languages, have dependencies, etc in place.  OSes have slow to roll out Rust packages & larger newer dependencies
        * CRob suggests to add this at a minimum as a risk to the plan.  The group may desire to take on this work as well.  Josh will file PR
* Brief talk about next steps to get our updates to the plan.
    * We will review the plan updates as a group, we can then circulate up to the BEST WG for comment, and then present to the TAC.  Mob Plan will begin formal rewrites later this year and then can simply use our revision as the new text.
* Josh would like to let folks here know about a memory safety event that ISRG’s Prossimo project is planning for November 2 in San Francisco. Day-long invite-only event building on previous discussions/events. We will skip the basics, spend time addressing a small set of critical open questions about shipping more memory safe code in software ecosystems. Let Josh know if you’re interested in attending! [josh@abetterinternet.org](mailto:josh@abetterinternet.org)
    * Can also ask the foundation to host a summit/webinar/workshop on the matter.  Could be low/no cost way to get maintainers and distros engaged
    * Consider targeting conferences and submit talks/panels to raise awareness/get engagement on implementing memory-safe languages and memory-safe programing techniques.
* Discussion on Rust Foundation new structure & adaption to growing pains

<h2>2023-06-08</h2>



<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
   <td>Pronouns
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>David A. Wheeler
   </td>
   <td>Linux Foundation
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Avishay Balter
   </td>
   <td>MIcrosoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Gabriel Dos Reis
   </td>
   <td>MIcrosoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>CRob
   </td>
   <td>Intel; TAC
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Daniel Frampton
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Jay White
   </td>
   <td>Microsoft
   </td>
   <td>
   </td>
  </tr>
</table>


Agenda



* Welcome new friends
* Help Scribe - David: I’ll help
* People haven’t had time to complete issues. Let’s give them time to make progress.

<h2>2023-05-25</h2>


Attendees:


<table>
  <tr>
   <td>Present?
   </td>
   <td>Name
   </td>
   <td>Organization
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>David A. Wheeler
   </td>
   <td>Linux Foundation
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Avishay Balter
   </td>
   <td>MIcrosoft
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Gabriel Dos Reis
   </td>
   <td>MIcrosoft
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>Mikey Strauss
   </td>
   <td>Scribe
   </td>
  </tr>
  <tr>
   <td>X
   </td>
   <td>CRob
   </td>
   <td>Intel, TAC
   </td>
  </tr>
</table>


 \
Agenda:



* Welcome new friends
* Help Scribe
* Discuss/approve drafts?
* We can walk through some open PRs [https://github.com/ossf/Memory-Safety/pulls](https://github.com/ossf/Memory-Safety/pulls) 
    * PR#4: [https://github.com/ossf/Memory-Safety/pull/4](https://github.com/ossf/Memory-Safety/pull/4) - WG decision today: Fix the markdown lint problems, then please merge. We'll track the TODOs as issues to close them out. David A. Wheeler will help with 3 (C/C++), CRob will help with 4 (education).
* David A. Wheeler: Question: Are techniques to improve memory safety in C/C++ in scope?
    * The Linux kernel is taking steps to counter *some* memory safety issues, e.g., Kees Cook “Bounded Flexible Arrays in C” [https://people.kernel.org/kees/bounded-flexible-arrays-in-c](https://people.kernel.org/kees/bounded-flexible-arrays-in-c). These can’t provide the same level of memory safety guarantee, as you can still easily write non-memory-safe code. But by applying certain practices you can counter specific kinds of memory safety problems (like buffer overflows). It’s okay if this is out-of-scope… it’s just best to make it clear what the group’s intended scope is.
    * See also: OpenSSF compiler flags work
    * See also: [https://discourse.llvm.org/t/rfc-enforcing-bounds-safety-in-c-fbounds-safety/70854](https://discourse.llvm.org/t/rfc-enforcing-bounds-safety-in-c-fbounds-safety/70854) 
    * Boost C++ library - safe pointers, etc. Warning: some organizations prohibit the use of Boost, primarily because it’s a huge monolith, some parts are actively maintained while others are vestigial and aren’t maintained. For example, some parts that are now obsolete as their functionality is part of C++ itself. See: [https://www.reddit.com/r/cpp/comments/gfowpq/why_you_dont_use_boost/](https://www.reddit.com/r/cpp/comments/gfowpq/why_you_dont_use_boost/)
        * David A. Wheeler: Historically LibreOffice had many different C++ types for strings, which created a huge overhead & made maintenance hard. Reducing library usage can help improve maintenance by simplifying the code. In short, a library to implement a function can be helpful, but having *multiple* libraries that implement the same functionality within an application can be a real problem.
    * Note: many items are dependent on specific hardware or specific compilers.
    * Yes, this is in scope.
    * Basically, this WG would create guide (or spec) for C/C++ to reduce the likelihood of memory safety problems in real-world applications. It’d note the above.
    * Maybe separate C from C++ guidance/spec.
* 

<h2>2023-04-27</h2>


Attendees:



* Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation)
* Gabriel Dos Reis (Microsoft)
* Jay White (Microsoft)
* Avishay Balter (Microsoft)
* David A. Wheeler (Linux Foundation)
* CRob (Intel)
* Charles C Palmer (IBM Research and Dartmouth)
* Matt Rutkowski (IBM)
* Randall T. Vasquez (LF/SKF/Gentoo)
* Jeff Borek (IBM)

Agenda



* Welcome new friends
* Scribe
* Discussion on revised wording of mobilization plan stream #4
    * Replace the wording for “known… vulnerabilities” to “classes of vulnerabilities”
    * Remove “known” as it may suggest purposeful action from developers
    * Should we add memory leaks
        * Java and C# can memory leak, but not in the same way as c/c++
        * However, memory leaks are an issue for some of the WG’s audience
    * Add link to NSA’s document on software memory safety
        * Switching to memory safe by default language, when possible
    * The emphasis should be what the language brings in terms of prevention, as opposed to name and blame specific technologies
    * Should the document reference specific tool or tool version or would that be too technical for the audience?
        * CRob suggests Mix people, process and tools
    * Discussion on declining suggestion for edit observing vulnerabilities in dependant code, since that relates more to SBOM/VEX and is handled by other WG/SIGs
* We want to have tooling that can prove memory safety in code, for instance in Scorecard.
    * Early discussion with Scorecard did not yet have a vision as to how that would look like in a Scorecard check. We should investigate on that more before reaching out again to the SC team
* We should expand the plan’s new items (3-5) and not only the original two points that were covered in the mobilization plan (MOVING CRITICAL SOFTWARE INFRASTRUCTURE TO MEMORY SAFE BY DEFAULT LANGUAGES and INVESTING IN SAFER SYSTEMS DEVELOPMENT TOOLS)
* We want to engage with other standard groups such as sigstore and Prossimo, through Josh to create an official liaison between the groups.
    * https://www.memorysafety.org/
    * We can work together with them, publish blogs together. 
    * Nell will reach out to Josh to setup this allyship between the SIG and the foundation’s work.
* [joke] Propose to have tin foil hat as the official logo and have stickers with that image for all! [/joke] 
* Next steps
    * Put together another draft.
    * Review the new draft revision.
    * Identity specific streams to work on and get funding on from the foundation.
    * Convert from GDoc to MD.

<h2>2023-04-13</h2>




* Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation)
* Gabriel Dos Reis (Microsoft)
* Jay White (Microsoft)
* Avishay Balter (Microsoft)
* David A. Wheeler (Linux Foundation)
* CRob (Intel)

Agenda



* [https://github.com/ossf/Memory-Safety/pull/1](https://github.com/ossf/Memory-Safety/pull/1)
    * Jordan is working to clean up GitHub permissions. In general we want to form teams, and then assign permissions to teams
* [https://docs.google.com/document/d/1e7-fUaPl1-uhXptsyD92MACvureXbMIUcmcD-ZyOd6M/edit](https://docs.google.com/document/d/1e7-fUaPl1-uhXptsyD92MACvureXbMIUcmcD-ZyOd6M/edit)
* Group agreed this initial SIG (co) leadership:
    * Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation) - @nellshamrell
    * Avishay Balter (Microsoft) - @balteravishay
* How do we define “memory safe language”
    * 
    * Key issue: “by default”.
    * We should try to reuse existing definitions.
    * [https://www.memorysafety.org/docs/memory-safety/](https://www.memorysafety.org/docs/memory-safety/) - Memory safety is a property of some programming languages that prevents programmers from introducing certain types of bugs related to how memory is used. Since memory safety bugs are often security issues, memory safe languages are more secure than languages that are not memory safe.
    * [Rina Diane Caballar definition (IEEE)](https://spectrum.ieee.org/memory-safe-programming-languages): “Memory safety is a feature of programming languages that prevents certain types of memory-access bugs, such as out-of-bounds reads and writes, and use-after-free bugs. In an app that manages a list of to-do items, for example, an out-of-bounds read could involve accessing the nonexistent sixth item in a list of five, while a use-after-free bug could involve accessing one of the items on an already deleted to-do list. These bugs could lead to accessing private data, corrupting data, or even executing code that isn’t part of a program.” [https://spectrum.ieee.org/memory-safe-programming-languages](https://spectrum.ieee.org/memory-safe-programming-languages)
    * Most languages are memory safe. Languages that are _not_ memory-safe include C, standard C++, Objective-C, Vala, Forth, Assembly, Machine language,.
    * Memory-safe languages include Rust, Go, Ada, Python, JavaScript, TypeScript, Ruby, and many others.
    * There’s a subset of C++ that can be enforced by rules that counters memory safety problems. E.g., no new/delete, can’t access beyond memory bounds, etc.
    * Gdr will work out a definition of “memory safe language”
* Also: Quote the various citations for %s of vulnerabilities due to memory safety
* We won’t be able to convert EVERYTHING to memory safe languages in any near term. However, we can encourage using them, as they eliminate problems at their source
* If you keep using C or C++, the compiler options work will help to counter some memory safety issues.
* Linux kernel experience: They’re adding Rust for device drivers. In practice, they’re finding they’re changing their C interfaces to make them safer for all, e.g., preferring interfaces that are read-only. Linux is also changing how they use C to reduce the likelihood of memory safety problems, which is different but helpful.
* It’s misleading to say “safe” languages - say “memory safe”
* 

<h2>2023-03-30</h2>


Attendees: 



* 
* Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation)
* Gabriel Dos Reis (Microsoft)
* Christine Abernathy (F5)
* Josh Aas (he/him, ISRG/Prossimo)
* CRob (he/him, Intel/OSSF)
* Jonathan Leitschuh (he/him) OpenSSF
* Jay White (Microsoft)
* Randall T. Vasquez (SKF/Gentoo)
* Walter Pearce (he/him, Rust Foundation Security Engineer)
* Avishay Balter (Microsoft)

Agenda



* We are officially part of the Developer Best Practices SIG!
* We have a shiny new Git Repo! Let’s plan how we fill this out!
    * [https://github.com/ossf/Memory-Safety](https://github.com/ossf/Memory-Safety)
    * Filling out Nell, Walter, Avishay
* Ideas for first project
    * Rewrite memory safety language in OSS Mobilization Plan https://8112310.fs1.hubspotusercontent-na1.net/hubfs/8112310/OpenSSF/OSS%20Mobilization%20Plan.pdf?hsCtaTracking=3b79d59d-e8d3-4c69-a67b-6b87b325313c%7C7a1a8b01-65ae-4bac-b97c-071dac09a2d8
    * Google doc - start with commenting?
        * Will create one after the meeting
* https://docs.google.com/document/d/1e7-fUaPl1-uhXptsyD92MACvureXbMIUcmcD-ZyOd6M/edit

<h2>2023-03-02</h2>


Attendees: 



* Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation)
* David A. Wheeler (Linux Foundation)
* Josh Aas (ISRG)
* Art Manion (self, contractor to but do not speak for CISA))
* Walter Pearce - Rust Foundation, focused on security
* Daniel Frampton (Microsoft)
* Randall T. Vasquez (SKF/Gentoo)
* Avishay Balter (Microsoft)
* Jay White (Microsoft)
* 

Agenda



* Further define goals as a SIG
    * This is not just a Rust group. The goal is to encourage memory safety. It includes how to make C/C++ better, since we can’t rewrite everything instantly.
    * We need to crisply define goal. Maybe start with mobilization plan.
    * The purpose of memory safety SIG is to encourage the transition to memory safe programming languages and approaches in open source software.
    * The purpose of memory safety SIG is to improve memory safety in OSS.
    * Develop and promote standards and guidelines for memory safe programming practices
    * Purpose: Eliminate memory safety vulnerabilities in OSS.
* Then define specific tasks to start, e.g., documents, programs, etc.
* Prep for presentation to Developer Best Practices WG [propose to join them?]

From [https://openssf.org/oss-security-mobilization-plan/](https://openssf.org/oss-security-mobilization-plan/):

Stream 4: Eliminate Root Causes of Many Vulnerabilities Through Replacement of Non-Memory-Safe Languages

Discussion about how to do this:



* Understanding factors that contribute to
    * Memory safety problems
    * Improvements
* Select and rewrite software (completely or modules) - e.g., Prossimo
* Remove roadblocks
    * CPU support
    * Inadequate performance of some languages
    * Difficulty in connecting with existing code (to enable incremental changes)
* Understand and document practical places to move away from memory unsafe languages
* Guidance, standards, practices, tools, advocacy
* Highlight successes, particularly running code
* Do we include/address confidential computing? Possibly a different class/layer of memory security problems?

Discussion on prevalence of memory-safety issues:



* Microsoft ~70%
* Chrome ~70%
* [https://advocacy.consumerreports.org/wp-content/uploads/2023/01/Memory-Safety-Convening-Report-1-1.pdf](https://advocacy.consumerreports.org/wp-content/uploads/2023/01/Memory-Safety-Convening-Report-1-1.pdf)
    * Alex Gaynor
* Across all NVD, ~25% (Art’s quick estimate with data with problems)
    * [https://docs.google.com/spreadsheets/d/1LlT_KusTuQSOka73Z3WUHHY1O0kcUuCnItA8wkX22L4](https://docs.google.com/spreadsheets/d/1LlT_KusTuQSOka73Z3WUHHY1O0kcUuCnItA8wkX22L4/edit#gid=0)
    * [https://noncombatant.org/2022/04/22/itw-taxonomy/](https://noncombatant.org/2022/04/22/itw-taxonomy/)

**Vision: Eliminate memory safety vulnerabilities (in Open Source Software (OSS).**

**Mission: Understand and reduce memory safety vulnerabilities in OSS.**

**Scope/Purpose: Develop pragmatic guidance, standards, and software (including tools, tool improvements, and rewrites), along with advocating such changes, to systematically reduce memory safety vulnerabilities through the use of memory-safe programming languages and techniques, all informed by real-world data and risks.**

Will present this to the Best Practices WG to be accepted.

Next meeting, 4 weeks from today - March 30. Keep talking on Slack.

we are in the OpenSSF Slack stream #stream-04-memory-safety channel

[https://join.slack.com/t/openssf/shared_invite/zt-1o4q7bq81-rZTF_3le_4B5wGWwvLYqoA](https://join.slack.com/t/openssf/shared_invite/zt-1o4q7bq81-rZTF_3le_4B5wGWwvLYqoA)

<h2>2023-xx-xx</h2>




* Nell Shamrell-Harrington (she/they, Microsoft, Rust Foundation)
* Gabriel Dos Reis (Microsoft)
* Jay White (Microsoft)
* Avishay Balter (Microsoft)
* David A. Wheeler (Linux Foundation)
* CRob (Intel)
* Charles C Palmer (IBM Research and Dartmouth)
* Randall T. Vasquez (LF/SKF/Gentoo)

Agenda



* Welcome new friends
* Scribe
* 
