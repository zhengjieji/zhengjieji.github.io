---
title: "Poster: Does Safe == Secure?: An Empirical Study of Vulnerabilities in Safe Rust"
collection: publications
category: abstracts
# permalink: /publication/2023-sp-threatkg
excerpt: 'Ruicheng Miao, Zhengjie Ji, Lingxiang Wang, Ruide Zhang, Ying Zhang.'
date: 2025-10-01
venue: 'USENIX Security Symposium'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
# paperurl: 'http://zhengjieji.github.io/files/2023-sp-threatkg.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Rust's ownership-based, compile-time memory safety guarantees and performance characteristics have led to its adoption in security-critical systems, including in foundational cloud services, operating systems, and IoT platforms. While prior research has focused on memory bugs in unsafe Rust, the security properties of safe Rust code have received less investigation.

This work presents a systematic analysis of vulnerabilities in safe Rust, based on a manually validated dataset of 135 RustSec advisories reported between 2021 and 2025. Our analysis identifies four primary risk categories. The first, logic flaws, such as inadequate input validation, can lead to vulnerabilities, including memory corruption and privilege escalation. The second category involves the misuse of dependencies, APIs, and configurations, which constitutes an attack surface with an observable increase in denial-of-service and cryptographic-failure incidents. The third category consists of compiler-related soundness issues, where aggressive optimizations can produce incorrect behavior in otherwise safe code. The fourth category involves incorrect lifetime and type annotations, which can inadvertently bypass the language's intended safety semantics. These findings show that compile-time guarantees do not eliminate run-time vulnerabilities; code designated as memory-safe is not necessarily secure. Our study sheds light on secure coding practices in safe Rust and provides pathways for compiler developers, library maintainers, and tool-chain builders to improve the security of the Rust ecosystem.