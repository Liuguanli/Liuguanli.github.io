---
layout: single
title: "About Me"
permalink: /
author_profile: true
---

I am a software engineer and postdoctoral researcher at the University of Melbourne. I work on scalable backend systems, data infrastructure, and performance-oriented data systems spanning ingestion, physical design, indexing, benchmarking, and retrieval. My research and engineering work has appeared in top database venues such as VLDB and ICDE, with a focus on reliability, scalability, debuggability, and efficient execution.

Previously, I worked as a Data Scientist at nftDb and as a Software Engineer at Baidu. Across research and industry, I have built end-to-end systems involving backend services, data pipelines, benchmarking frameworks, query optimization components, and retrieval workflows. I am based in Melbourne, Australia, and open to remote and relocation opportunities.

[CV](/cv/CV.pdf)

### What I Work On

- **Data layout and physical design**: layout advisory systems, SQL workload parsing, and efficient cost models for data lake style datasets.
- **Benchmarking and evaluation**: frameworks for measuring performance stability, drift sensitivity, latency, and I/O behavior across indexing and database tuning workloads.
- **Indexing and retrieval systems**: learned indexes, spatial index structures, vector retrieval pipelines, and LLM-assisted query processing.
- **Production data engineering**: ingestion pipelines, batch and streaming workflows, analytics modeling, and backend services for data-intensive products.

### Selected Projects

#### Layout Advisor

<img src="/images/projects/layout-advisor.svg" alt="Layout Advisor overview" width="100%">

Advisory system for dataset ingestion, workload parsing, and layout recommendation for data lake workloads. [Code](https://github.com/Liuguanli/layout_advisor)

#### DriftBench

<img src="/images/projects/driftbench.svg" alt="DriftBench overview" width="100%">

Framework for evaluating performance stability under workload drift and data drift in benchmarking and tuning scenarios. [Code](https://github.com/Liuguanli/DriftBench) | [Paper](https://arxiv.org/abs/2510.10858)

#### RSMI

<img src="/images/projects/rsmi.svg" alt="RSMI overview" width="100%">

Recursive learned spatial index structures for multidimensional query workloads. [Code](https://github.com/Liuguanli/RSMI) | [Paper](https://www.vldb.org/pvldb/vol13/p2341-qi.pdf)

**More projects**

- **LBMC**: file layout method with an `O(1)` cost model for evaluating layout quality efficiently. [Code](https://github.com/Liuguanli/LBMC) | [Paper](https://www.vldb.org/pvldb/vol17/p4773-liu.pdf)
- **RL Spatial Benchmark**: benchmarking framework for traditional and learned spatial indexes under controlled query workloads. [Code](https://github.com/Liuguanli/rl_spatial_benchmark) | [Paper](https://arxiv.org/abs/2512.11161)

### Selected Publications

- **Guanli Liu**, Renata Borovica-Gajic, Hai Lan, Zhifeng Bao. *Benchmarking RL-Enhanced Spatial Indices Against Traditional, Advanced, and Learned Counterparts*. ICDE 2026.
- Lankadinee Rathuwadu, **Guanli Liu**, Christopher Leckie, Renata Borovica-Gajic. *CoLSE: A Lightweight and Robust Hybrid Learned Model for Single-Table Cardinality Estimation using Joint CDF*. ICDE 2026.
- **Guanli Liu**, Lars Kulik, Christian S. Jensen, Tianyi Li, Renata Borovica-Gajic, Jianzhong Qi. *Efficient Cost Modeling of Space-filling Curves*. VLDB 2025.
- **Guanli Liu**, Jianzhong Qi, Lars Kulik, Kazuya Soga, Renata Borovica-Gajic, Benjamin I. P. Rubinstein. *Efficient Index Learning via Model Reuse and Fine-tuning*. ICDEW 2023. [Paper](https://people.eng.unimelb.edu.au/jianzhongq/papers/DBML2023_ModelReuse.pdf)
- **Guanli Liu**, Jianzhong Qi, Christian S. Jensen, James Bailey, Lars Kulik. *Efficiently Learning Spatial Indices*. ICDE 2023. [Paper](https://people.eng.unimelb.edu.au/baileyj/papers/ICDE2023_ELSI.pdf)
- Jianzhong Qi, **Guanli Liu**, Christian S. Jensen, Lars Kulik. *Effectively Learning Spatial Indices*. PVLDB 2020. [Paper](https://www.vldb.org/pvldb/vol13/p2341-qi.pdf)

### Experience

- **Postdoctoral Research Fellow / PhD Researcher**, The University of Melbourne, 2019-Present
- **Data Scientist**, nftDb, 2023-2024
- **Software Engineer**, Baidu, 2015-2017

### Skills

- **Languages**: Python, Java, C++, SQL
- **Data Systems**: PostgreSQL, PostGIS, pgvector, BigQuery, SparkSQL, Apache Hudi
- **Pipelines and Infrastructure**: Kafka, Airflow, dbt, REST APIs, Docker, Google Cloud Platform
- **AI and Retrieval**: RAG pipelines, vector databases, embedding-based retrieval, PyTorch, scikit-learn

### Teaching and Service

- **Teaching**: Tutor for COMP90018 Android Application Development and COMP90041 Programming and Software Development at the University of Melbourne.
- **Research Service**: Reviewer for SIGMOD, VLDB, KDD, TKDE, WWW, and TSAS.
