---
title: "BPFflow - Preventing information leaks from eBPF"
collection: publications
category: conferences
permalink: /publication/2025-ebpf-bpfflow
excerpt: 'Chinecherem Dimobi, Rahul Tiwari, Zhengjie Ji, Dan Williams.'
date: 2025-10-01
venue: 'Workshop on eBPF and Kernel Extensions'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'http://zhengjieji.github.io/files/2025-ebpf-bpfflow.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
eBPF has seen major industry adoption by enterprises to enhance observability, tracing and monitoring by hooking at different points in the kernel. However, since the kernel is a critical resource, eBPF can also pose as a threat if misused, potentially leading to privilege escalation, information leaks and more. While effective to some extent, existing mitigation strategies like interface filtering are coarse-grained and often over-restrictive.

We propose BPFflow, a flexible framework for the system administrator to define policies that specify sensitive data sources, trusted sinks, and permitted flows between them. These policies are enforced by an Information Flow Control (IFC) system within the eBPF verifier to track the propagation of sensitive data to prevent unauthorized leakage to userspace or any other untrusted sinks without any runtime overhead.