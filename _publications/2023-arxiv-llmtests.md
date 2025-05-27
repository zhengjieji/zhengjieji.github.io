---
title: "How well does LLM generate security tests?"
collection: publications
category: conferences
permalink: /publication/2023-arxiv-llmtests
excerpt: 'Ying Zhang, Wenjia Song, Zhengjie Ji, Daphne Yao, Na Meng.'
date: 2023-10-01
venue: 'CoRR arXiv'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'http://zhengjieji.github.io/files/2023-arxiv-llmtests.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Developers often build software on top of third-party libraries (Libs) to improve programmer productivity and software quality. The libraries may contain vulnerabilities exploitable by hackers to attack the applications (Apps) built on top of them. People refer to such attacks as supply chain attacks, the documented number of which has increased 742% in 2022. People created tools to mitigate such attacks, by scanning the library dependencies of Apps, identifying the usage of vulnerable library versions, and suggesting secure alternatives to vulnerable dependencies. However, recent studies show that many developers do not trust the reports by these tools; they ask for code or evidence to demonstrate how library vulnerabilities lead to security exploits, in order to assess vulnerability severity and modification necessity. Unfortunately, manually crafting demos of application-specific attacks is challenging and time-consuming, and there is insufficient tool support to automate that procedure.

In this study, we used ChatGPT-4.0 to generate security tests, and to demonstrate how vulnerable library dependencies facilitate the supply chain attacks to given Apps. We explored various prompt styles/templates, and found that ChatGPT-4.0 generated tests for all 55 Apps, demonstrating 24 attacks successfully. It outperformed two state-of-the-art security test generators -- TRANSFER and SIEGE -- by generating a lot more tests and achieving more exploits. ChatGPT-4.0 worked better when prompts described more on the vulnerabilities, possible exploits, and code context. Our research will shed light on new research in security test generation. The generated tests will help developers create secure by design and secure by default software.