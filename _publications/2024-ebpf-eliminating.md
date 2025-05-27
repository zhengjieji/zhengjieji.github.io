---
title: "Eliminating eBPF Tracing Overhead on Untraced Processes"
collection: publications
category: conferences
permalink: /publication/2024-ebpf-eliminating
excerpt: 'Milo Craun, Khizar Hussain, Uddhav Gautam, Zhengjie Ji, Tanuj Rao, Dan Williams.'
date: 2024-08-04
venue: 'Workshop on eBPF and Kernel Extensions'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'http://zhengjieji.github.io/files/2024-ebpf-eliminating.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Current eBPF-based kernel extensions affect entire systems, and are coarse-grained. For some use cases, like tracing, operators are more interested in tracing a subset of processes (e.g., belonging to a container) rather than all processes. While overhead from tracing is expected for targeted processes, we find untraced processes---those that are not the target of tracing---also incur performance overhead. To better understand this overhead, we identify and explore three techniques for per-process filtering for eBPF: post-eBPF, in-eBPF, and pre-eBPF filtering, finding that all three approaches result in excessive overhead on untraced processes. Finally, we propose a system that allows for zero-untraced-overhead per-process eBPF tracing by modifying kernel virtual memory mappings to present per-process kernel views, effectively enabling untraced processes to execute on the kernel as if no eBPF programs are attached.