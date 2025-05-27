---
title: "PrivMon: A Stream-Based System for Real-Time Privacy Attack Detection for Machine Learning Models"
collection: publications
category: conferences
permalink: /publication/2023-raid-privmon
excerpt: 'Myeongseob Ko, Xinyu Yang, Zhengjie Ji, Hoang Anh Just, Peng Gao, Anoop Kumar, Ruoxi Jia.'
date: 2023-08-04
venue: 'International Symposium on Research in Attacks, Intrusions and Defenses'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'http://zhengjieji.github.io/files/2023-raid-privmon.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Machine learning (ML) models can expose the private information of training data when confronted with privacy attacks. Specifically, a malicious user with black-box access to a ML-as-a-service platform can reconstruct the training data (i.e., model inversion attacks) or infer the membership information (i.e., membership inference attacks) simply by querying the ML model. Despite the pressing need for effective defenses against privacy attacks with black-box access, existing approaches have mostly focused on enhancing the robustness of the ML model via modifying the model training process or the model prediction process. These defenses can compromise model utility and require the cooperation of the underlying AI platform (i.e., platform-dependent). These constraints largely limit the real-world applicability of existing defenses.

Despite the prevalent focus on improving the model’s robustness, none of the existing works have focused on the continuous protection of already deployed ML models from privacy attacks by detecting privacy leakage in real-time. This defensive task becomes increasingly important given the vast deployment of ML-as-a-service platforms these days. To bridge the gap, we propose PrivMon, a new stream-based system for real-time privacy attack detection for ML models. To facilitate wide applicability and practicality, PrivMon defends black-box ML models against a wide range of privacy attacks in a platform-agnostic fashion: PrivMon only passively monitors model queries without requiring the cooperation of the model owner or the AI platform. Specifically, PrivMon takes as input a stream of ML model queries and provides an efficient attack detection engine that continuously monitors the stream to detect the privacy attack in real-time, by identifying self-similar malicious queries. We show empirically and theoretically that PrivMon can detect a wide range of realistic privacy attacks within a practical time frame and successfully mitigate the attack success rate. Code is available at https://github.com/ruoxi-jia-group/privmon.