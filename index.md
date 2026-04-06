---
layout: single
title: "About Me"
permalink: /
author_profile: true
---

I am a software engineer and postdoctoral researcher at the University of Melbourne. I work on scalable backend systems, data infrastructure, and performance-oriented data systems spanning ingestion, physical design, indexing, benchmarking, and retrieval. My research and engineering work has appeared in top database venues such as VLDB and ICDE, with a focus on reliability, scalability, debuggability, and efficient execution.

Previously, I worked as a Data Scientist at nftDb and as a Software Engineer at Baidu. Across research and industry, I have built end-to-end systems involving backend services, data pipelines, benchmarking frameworks, query optimization components, and retrieval workflows. I am based in Melbourne, Australia, and open to remote and relocation opportunities.

### What I Work On

- **Data layout and physical design**: layout advisory systems, SQL workload parsing, and efficient cost models for data lake style datasets.
- **Benchmarking and evaluation**: frameworks for measuring performance stability, drift sensitivity, latency, and I/O behavior across indexing and database tuning workloads.
- **Indexing and retrieval systems**: learned indexes, spatial index structures, vector retrieval pipelines, and LLM-assisted query processing.
- **Production data engineering**: ingestion pipelines, batch and streaming workflows, analytics modeling, and backend services for data-intensive products.

### Selected Projects

#### LayoutPilot / Layout Advisory

<img src="/images/projects/layoutpilot-paper.png" alt="LayoutPilot figure from paper" style="width: 325px; max-width: 42%; float: right; margin: 0.15rem 0 1rem 1.5rem; padding: 0.35rem; border: 1px solid #e5e7eb; border-radius: 8px; background: #fff;">

An interactive, workload-aware advisor for single-table lakehouse physical design at ingestion time. Given a dataset and target workload, it analyzes data characteristics, workload signals, and column correlations to recommend partitioning and intra-file layout choices before poor physical design decisions degrade query performance.

The system is designed to make recommendations explainable rather than opaque: users can inspect recommendation evidence, compare candidate designs, and validate whether estimated rankings align with observed query behavior.

**Links:** [Code](https://github.com/Liuguanli/layout_advisor) | [Paper](/papers/layoutpilot-vldb-demo-2026.pdf)

<div style="clear: both;"></div>

#### DriftBench

<img src="/images/projects/driftbench-paper.png" alt="DriftBench figure from paper" style="width: 285px; max-width: 37%; float: right; margin: 0.15rem 0 1rem 1.5rem; padding: 0.35rem; border: 1px solid #e5e7eb; border-radius: 8px; background: #fff;">

A drift-aware benchmarking framework built around a taxonomy of data drift and workload drift, plus a declarative specification layer, `DriftSpec`, for making drift scenarios executable and reproducible. It supports controlled generation of evolving data and workloads so that database components can be evaluated beyond static, one-off benchmark runs.

The goal is to shift benchmarking toward continuous evaluation under change, making it easier to study robustness, stability, and adaptation in systems such as cardinality estimators, indexing methods, and query optimizers.

**Links:** [Code](https://github.com/Liuguanli/DriftBench) | [Paper](https://arxiv.org/abs/2510.10858)

<div style="clear: both;"></div>

### Selected Publications

- **Guanli Liu**, Renata Borovica-Gajic, Hai Lan, Zhifeng Bao. *Benchmarking RL-Enhanced Spatial Indices Against Traditional, Advanced, and Learned Counterparts*. ICDE 2026.
- Lankadinee Rathuwadu, **Guanli Liu**, Christopher Leckie, Renata Borovica-Gajic. *CoLSE: A Lightweight and Robust Hybrid Learned Model for Single-Table Cardinality Estimation using Joint CDF*. ICDE 2026.
- **Guanli Liu**, Lars Kulik, Christian S. Jensen, Tianyi Li, Renata Borovica-Gajic, Jianzhong Qi. *Efficient Cost Modeling of Space-filling Curves*. VLDB 2025.
- **Guanli Liu**, Jianzhong Qi, Lars Kulik, Kazuya Soga, Renata Borovica-Gajic, Benjamin I. P. Rubinstein. *Efficient Index Learning via Model Reuse and Fine-tuning*. ICDEW 2023. [Paper](https://people.eng.unimelb.edu.au/jianzhongq/papers/DBML2023_ModelReuse.pdf)
- **Guanli Liu**, Jianzhong Qi, Christian S. Jensen, James Bailey, Lars Kulik. *Efficiently Learning Spatial Indices*. ICDE 2023. [Paper](https://people.eng.unimelb.edu.au/baileyj/papers/ICDE2023_ELSI.pdf)
- Jianzhong Qi, **Guanli Liu**, Christian S. Jensen, Lars Kulik. *Effectively Learning Spatial Indices*. PVLDB 2020. [Paper](https://www.vldb.org/pvldb/vol13/p2341-qi.pdf)

### Research and Work Experience

- **PhD + Postdoc, The University of Melbourne, Australia**, June 2019-Present  
  Lead research and engineering projects on database benchmarking, indexing, and AI-driven query processing. Design system prototypes, supervise junior researchers, and collaborate with academic and industry partners.
- **Data Scientist, nftDb, Australia**, Feb. 2023-Feb. 2024  
  Built Python-based ingestion pipelines for raw blockchain transaction data, supporting Kafka-based streaming and Airflow-orchestrated batch workflows for downstream analytics. Developed SQL and dbt workflows to clean, normalize, and model large-scale transaction data into analytics-ready tables for product insights and reporting. Queried and analyzed transaction-level datasets in BigQuery, and developed an internal RAG-based knowledge assistant for documentation retrieval, data asset discovery, and workflow support across engineering teams.
- **Software Engineer, Baidu, China**, Jul. 2015-Aug. 2017  
  Worked on Baidu's IM platform serving employees and business partners. Designed messaging protocols and implemented message deduplication mechanisms to improve delivery reliability and consistency across large-scale communication workflows. Improved database performance through profiling, query optimization, and systematic tuning of backend data access workflows.

### Engineering Skills

- **Programming**: Proficient in Python and Java, with working knowledge of C++ and SQL
- **Data Systems and Pipelines**: Experience with SparkSQL, Apache Hudi, REST APIs, data ingestion pipelines, and batch / incremental data processing
- **Databases**: Experience with PostgreSQL, PostGIS, pgvector, BigQuery, and spatial data management
- **AI / Retrieval Systems**: Experience with RAG pipelines, vector databases, embedding-based retrieval
- **Cloud and Infrastructure**: Experience with Google Cloud Platform and Docker
- **Machine Learning**: Hands-on experience with PyTorch, TorchLib, Scikit-learn, and common machine learning algorithms for classification, regression, clustering, and representation learning
- **Algorithmic Knowledge**: Solid understanding of fundamental data structures and algorithms

### Education

- **PhD in Computer Science**, The University of Melbourne, Australia, 2019-2023
- **M.S. in Computer Technology**, Northeastern University, China, 2013-2015
- **B.Eng. in Software Engineering**, Northeastern University, China, 2009-2013

### Teaching

- **COMP90018 - Android Application Development (The University of Melbourne)**: Tutor from Aug. 2019 to 2023, responsible for tutorials, student support, and assessment marking.
- **COMP90041 - Programming and Software Development (The University of Melbourne)**: Tutor from Aug. 2019 to 2023, responsible for tutorials and assessment marking.

### Research Service

- **Conference Reviewer**: SIGMOD 2026, VLDB 2027 (PC), VLDB 2026 (Shadow PC), VLDB 2025 (External), KDD 2026, KDD 2025 (Excellent Reviewer)
- **Journal Reviewer**: TKDE, WWW, Transactions on Spatial Algorithms and Systems (TSAS)
