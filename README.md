## Guanli Liu

<div align="left">
  <img src="./image/head.png" alt="Guanli Liu" style="width: 120px; height: 128px; float: right; margin: 10px">
  <p><strong>Software Engineer · Data Systems · AI for Databases</strong></p>
  <p>
    I am a software engineer and postdoctoral researcher at the University of Melbourne. I build scalable backend systems, data infrastructure, and performance-oriented data systems spanning ingestion, physical design, indexing, benchmarking, and retrieval. My research and engineering work has appeared in top database venues such as VLDB and ICDE, with a strong focus on reliability, scalability, debuggability, and efficient execution.
  </p>
  <p>
    Previously, I worked as a Data Scientist at nftDb and as a Software Engineer at Baidu. Across research and industry, I have delivered end-to-end systems involving backend services, data pipelines, benchmarking frameworks, query optimization components, and retrieval workflows. I am based in Melbourne, Australia, and open to remote and relocation opportunities.
  </p>
</div>

[CV](./cv/CV.pdf) · [LinkedIn](https://www.linkedin.com/in/guanli-liu-11353058/) · [GitHub](https://github.com/Liuguanli) · [Email](mailto:liuguanli22@gmail.com)

---

### Contact

- Location: Melbourne, Australia
- Timezone: UTC+10 / UTC+11
- Email: [liuguanli22@gmail.com](mailto:liuguanli22@gmail.com)

---

### What I Work On

- **Data layout and physical design**: building layout advisory systems, SQL workload parsers, and cost models for data lake style datasets.
- **Benchmarking and evaluation**: designing frameworks to measure stability, drift sensitivity, latency, and I/O behavior across indexing and database tuning workloads.
- **Indexing and retrieval systems**: developing learned indexes, spatial index structures, vector retrieval workflows, and LLM-assisted query processing systems.
- **Production data engineering**: building ingestion pipelines, batch and streaming workflows, analytics models, and backend services for data-intensive applications.

---

### Selected Projects

- **Layout Advisor**: end-to-end advisory system for dataset ingestion, workload parsing, and layout recommendation for data lake workloads. [Code](https://github.com/Liuguanli/layout_advisor) · [Paper](./papers/layoutpilot-vldb-demo-2026.pdf)
- **LBMC**: file layout method with an `O(1)` cost model for evaluating layout quality efficiently. [Code](https://github.com/Liuguanli/LBMC) · [Paper](https://www.vldb.org/pvldb/vol17/p4773-liu.pdf)
- **DriftBench**: framework for evaluating performance stability under workload and data drift in benchmarking and tuning scenarios. [Code](https://github.com/Liuguanli/DriftBench) · [Paper](https://arxiv.org/abs/2510.10858)
- **RL Spatial Benchmark**: benchmarking framework for traditional and learned spatial indexes under controlled query workloads. [Code](https://github.com/Liuguanli/rl_spatial_benchmark) · [Paper](https://arxiv.org/abs/2512.11161)
- **RSMI**: recursive learned spatial index structures for multidimensional query workloads. [Code](https://github.com/Liuguanli/RSMI) · [Paper](https://www.vldb.org/pvldb/vol13/p2341-qi.pdf)
- **Complex Spatial Query Generation**: supervised project on LLM-assisted processing of complex spatial queries. [Code](https://github.com/AI-DB-UoM/complex_spatial_data_generation)

---

### Selected Publications

- **Guanli Liu**, Renata Borovica-Gajic, Hai Lan, Zhifeng Bao. *Benchmarking RL-Enhanced Spatial Indices Against Traditional, Advanced, and Learned Counterparts*. ICDE 2026.
- Lankadinee Rathuwadu, **Guanli Liu**, Christopher Leckie, Renata Borovica-Gajic. *CoLSE: A Lightweight and Robust Hybrid Learned Model for Single-Table Cardinality Estimation using Joint CDF*. ICDE 2026.
- **Guanli Liu**, Lars Kulik, Christian S. Jensen, Tianyi Li, Renata Borovica-Gajic, Jianzhong Qi. *Efficient Cost Modeling of Space-filling Curves*. VLDB 2025.
- **Guanli Liu**, Jianzhong Qi, Lars Kulik, Kazuya Soga, Renata Borovica-Gajic, Benjamin I. P. Rubinstein. *Efficient Index Learning via Model Reuse and Fine-tuning*. ICDEW 2023. [Paper](https://people.eng.unimelb.edu.au/jianzhongq/papers/DBML2023_ModelReuse.pdf)
- **Guanli Liu**, Jianzhong Qi, Christian S. Jensen, James Bailey, Lars Kulik. *Efficiently Learning Spatial Indices*. ICDE 2023. [Paper](https://people.eng.unimelb.edu.au/baileyj/papers/ICDE2023_ELSI.pdf)
- Jianzhong Qi, **Guanli Liu**, Christian S. Jensen, Lars Kulik. *Effectively Learning Spatial Indices*. PVLDB 2020. [Paper](https://www.vldb.org/pvldb/vol13/p2341-qi.pdf)

---

### Experience

- **Postdoctoral Research Fellow / PhD Researcher**, The University of Melbourne, 2019-Present  
  Leading research and engineering projects on database benchmarking, indexing, data layout, and AI-driven query processing.
- **Data Scientist**, nftDb, 2023-2024  
  Built blockchain ingestion pipelines, dbt and SQL analytics workflows, BigQuery-based analysis, and an internal RAG assistant for engineering knowledge retrieval.
- **Software Engineer**, Baidu, 2015-2017  
  Worked on large-scale messaging systems, message deduplication, and database performance optimization for internal communication platforms.

---

### Skills

- **Languages**: Python, Java, C++, SQL
- **Data Systems**: PostgreSQL, PostGIS, pgvector, BigQuery, SparkSQL, Apache Hudi
- **Pipelines and Infrastructure**: Kafka, Airflow, dbt, REST APIs, Docker, Google Cloud Platform
- **AI and Retrieval**: RAG pipelines, vector databases, embedding-based retrieval, PyTorch, scikit-learn
- **Focus Areas**: backend systems, data infrastructure, benchmarking, query processing, learned indexes, spatial data systems

---

### Teaching and Service

- **Teaching**: Tutor for COMP90018 Android Application Development and COMP90041 Programming and Software Development at the University of Melbourne.
- **Research Service**: Reviewer for SIGMOD, VLDB, KDD, TKDE, WWW, and TSAS.

---

### Building the CV PDFs

This repository includes multiple LaTeX CV variants under [`cv/`](./cv/). To build them locally:

```bash
cd cv
make            # build every *.tex into a PDF
make watch      # live rebuild the default CV while editing
make clean      # remove auxiliary files
make distclean  # remove auxiliary files and PDFs
```

To watch a specific CV file:

```bash
cd cv
make watch DEFAULT_TEX=CV-ML.tex
```
