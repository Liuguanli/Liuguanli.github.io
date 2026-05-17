---
layout: single
title: "Portfolio"
permalink: /
author_profile: false
---

<style>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');

:root {
  --bg: #f5f5ef;
  --paper: #fffef8;
  --ink: #1f2a30;
  --muted: #4f5f66;
  --line: #c8d0c8;
  --accent: #0c7f63;
  --accent-2: #d97b2d;
  --soft: #eaf2ec;
}

@media (min-width: 57.8125em) {
  #main,
  .masthead__inner-wrap,
  .breadcrumbs {
    max-width: 1320px;
  }

  .page {
    float: none;
    width: 100%;
    margin: 0 auto;
    padding-left: 0;
    padding-right: 0;
  }
}

.page__content {
  font-family: "IBM Plex Sans", "Segoe UI", sans-serif;
  color: var(--ink);
}

.page__content p,
.page__content li {
  color: var(--muted);
  line-height: 1.7;
}

.page__title {
  display: none;
}

.portfolio-hero {
  margin: 0 0 2.2rem;
  padding: 3.6rem 2rem 3rem;
  background:
    radial-gradient(circle at 86% 22%, rgba(217, 123, 45, 0.2), transparent 40%),
    linear-gradient(150deg, #f2f1e8 0%, #dceae2 52%, #e9f2ee 100%);
  border-bottom: 1px solid #b9c8be;
  border-radius: 16px;
}

.portfolio-hero__layout {
  display: grid;
  grid-template-columns: 200px minmax(0, 1fr);
  gap: 1.6rem;
  align-items: center;
}

.portfolio-hero__portrait {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  overflow: hidden;
  border: 2px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 12px 28px rgba(16, 34, 36, 0.14);
  background: #ffffff;
}

.portfolio-hero__portrait img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.portfolio-hero__kicker {
  margin: 0 0 0.8rem;
  font-size: 0.82rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: #476054;
  font-weight: 700;
}

.portfolio-hero h1 {
  margin: 0;
  font-family: "Space Grotesk", "IBM Plex Sans", sans-serif;
  font-size: clamp(2rem, 5.6vw, 3.6rem);
  line-height: 1.05;
  color: #162329;
}

.portfolio-hero__lead {
  margin: 1rem 0 1.6rem;
  max-width: 820px;
  font-size: 1.05rem;
  color: #2f434b;
}

.portfolio-hero__cta {
  display: flex;
  flex-wrap: wrap;
  gap: 0.65rem;
}

.portfolio-hero__cta a {
  display: inline-block;
  padding: 0.5rem 0.88rem;
  border: 1px solid #90a397;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.65);
  color: #19313b;
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 600;
  transition: transform 0.22s ease, background 0.22s ease, border-color 0.22s ease;
}

.portfolio-hero__cta a:hover {
  transform: translateY(-2px);
  border-color: #446e5d;
  background: #ffffff;
}

.portfolio-section {
  margin: 2.25rem 0;
}

.portfolio-section h2 {
  margin-bottom: 0.6rem;
  font-family: "Space Grotesk", "IBM Plex Sans", sans-serif;
  color: #172a30;
  font-size: clamp(1.35rem, 2.8vw, 1.95rem);
}

.portfolio-section__note {
  margin: 0 0 1rem;
  color: #455862;
}

.track-list {
  border-top: 1px solid var(--line);
}

.track-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--line);
  display: grid;
  gap: 0.45rem;
}

.track-item strong {
  color: #1c343d;
  font-size: 1.03rem;
}

.case-list {
  border-top: 1px solid var(--line);
}

.case-item {
  padding: 1.15rem 0 1.3rem;
  border-bottom: 1px solid var(--line);
  display: grid;
  gap: 0.9rem;
}

.case-item--featured {
  margin-top: 0.7rem;
  padding: 1.1rem 1rem 1.3rem;
  border: 1px solid #98c8b7;
  border-radius: 14px;
  background: linear-gradient(155deg, #ffffff 0%, #eef8f3 100%);
}

.case-item__meta {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  font-size: 0.8rem;
}

.case-item__meta span {
  display: inline-block;
  padding: 0.18rem 0.5rem;
  border-radius: 999px;
  background: var(--soft);
  color: #21453b;
  border: 1px solid #cad9ce;
}

.case-item__title {
  margin: 0;
  font-family: "Space Grotesk", "IBM Plex Sans", sans-serif;
  color: #11262e;
}

.case-item__grid {
  display: grid;
  gap: 1rem;
}

.case-item__media img {
  display: block;
  width: 100%;
  max-width: 460px;
  border: 1px solid #d8ddd8;
  border-radius: 12px;
  background: #ffffff;
}

.case-item__links {
  font-size: 0.93rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.case-item__links a,
.link-pill {
  display: inline-block;
  padding: 0.26rem 0.62rem;
  border: 1px solid #bad5c7;
  border-radius: 999px;
  background: #ffffff;
  font-weight: 600;
  color: var(--accent);
  text-decoration: none;
}

.case-item__links a:hover,
.link-pill:hover {
  border-color: #4e8d77;
  text-decoration: none;
}

.link-pill--primary {
  background: #0c7f63;
  border-color: #0b745b;
  color: #ffffff !important;
}

.publication-list {
  border-top: 1px solid var(--line);
}

.publication-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--line);
  display: grid;
  gap: 0.45rem;
}

.publication-item__title {
  margin: 0;
  color: #1c343d;
  font-size: 1.02rem;
}

.publication-item__meta {
  font-size: 0.9rem;
}

.publication-item__links {
  font-size: 0.9rem;
}

.publication-item__links a {
  color: var(--accent);
  text-decoration: none;
  font-weight: 600;
}

.publication-item__links a:hover {
  text-decoration: underline;
}

.publication-badge {
  display: inline-block;
  margin-left: 0.45rem;
  padding: 0.1rem 0.42rem;
  border-radius: 999px;
  border: 1px solid #cad9ce;
  background: var(--soft);
  color: #21453b;
  font-size: 0.74rem;
  font-weight: 600;
  vertical-align: middle;
}

.build-queue {
  padding: 1rem 1.1rem;
  border: 1px solid #cfdbd3;
  border-radius: 14px;
  background: linear-gradient(155deg, #ffffff 0%, #f2f8f4 100%);
}

.build-queue ul {
  margin: 0.5rem 0 0;
}

.timeline {
  margin-top: 0.5rem;
  border-left: 2px solid #b8c7bc;
  padding-left: 1rem;
}

.timeline p {
  margin: 0 0 0.75rem;
}

.experience-item {
  margin: 0 0 1rem;
}

.experience-item p {
  margin: 0.35rem 0;
}

.teaching-service-card {
  padding: 1rem 1.1rem;
  border: 1px solid #cfdbd3;
  border-radius: 14px;
  background: #ffffff;
}

.teaching-service-card h3 {
  margin: 0.2rem 0 0.5rem;
  font-family: "Space Grotesk", "IBM Plex Sans", sans-serif;
  color: #172a30;
}

.teaching-service-card ul {
  margin-top: 0.25rem;
}

.fade-up {
  opacity: 0;
  transform: translateY(12px);
  animation: fadeUp 0.7s ease forwards;
}

.fade-up:nth-child(2) { animation-delay: 0.08s; }
.fade-up:nth-child(3) { animation-delay: 0.16s; }
.fade-up:nth-child(4) { animation-delay: 0.24s; }

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (min-width: 57.8125em) {
  .case-item__grid {
    grid-template-columns: minmax(0, 1fr) 320px;
    align-items: start;
  }
}

@media (max-width: 57.8124em) {
  .portfolio-hero {
    margin-bottom: 1.6rem;
    padding: 2.4rem 1.2rem 2.2rem;
  }

  .portfolio-hero__layout {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .portfolio-hero__portrait {
    width: 132px;
    height: 132px;
  }

  .portfolio-hero h1 {
    font-size: clamp(1.8rem, 9.5vw, 3rem);
  }
}
</style>

<section class="portfolio-hero">
  <div class="portfolio-hero__layout">
    <figure class="portfolio-hero__portrait fade-up">
      <img src="/images/head.png" alt="Portrait of Guanli Liu">
    </figure>
    <div>
      <p class="portfolio-hero__kicker fade-up">Guanli (Leo) Liu · Backend Systems · Data Infrastructure · Research Engineering</p>
      <h1 class="fade-up">I build data and AI systems, then turn them into reproducible, measurable products.</h1>
      <p class="portfolio-hero__lead fade-up">
        Postdoctoral researcher and engineer at the University of Melbourne. This site is organized as a growing portfolio of case studies across database systems, benchmarking, and LLM-assisted data workflows.
      </p>
      <div class="portfolio-hero__cta fade-up">
        <a href="/cv/resume.pdf">View CV</a>
        <a href="https://github.com/Liuguanli">GitHub</a>
        <a href="https://www.linkedin.com/in/guanli-liu/">LinkedIn</a>
        <a href="https://scholar.google.com/citations?hl=en&user=7e89UC8AAAAJ&view_op=list_works&sortby=pubdate">Google Scholar</a>
        <a href="mailto:liuguanli22@gmail.com">Email</a>
      </div>
    </div>
  </div>
</section>

<section class="portfolio-section">
  <h2>Research & Engineering Focus</h2>
  <p class="portfolio-section__note">Current focus areas linked to active systems, papers, and open-source delivery.</p>
  <div class="track-list">
    <article class="track-item">
      <strong>Drift-Aware Benchmarking Systems</strong>
      <span>DriftBench and AI-DB benchmark workflows for reproducible workload and data drift evaluation.</span>
    </article>
    <article class="track-item">
      <strong>PostgreSQL Extension Intelligence</strong>
      <span>Extension-oriented benchmarking and integration of HMAB, GRASP, and CoLSE in a unified AI-DB runtime.</span>
    </article>
    <article class="track-item">
      <strong>Data Layout and Query Performance</strong>
      <span>Lakehouse physical design, indexing, and cost-aware optimization for analytical workloads.</span>
    </article>
    <article class="track-item">
      <strong>LLM-Assisted Database Workflows</strong>
      <span>Natural language to executable query pipelines with retrieval, decomposition, and result-grounded checks.</span>
    </article>
    <article class="track-item">
      <strong>Open-Source Product Delivery</strong>
      <span>GitHub-first development, PyPI releases, documentation websites, and repeatable CI/CD workflows.</span>
    </article>
  </div>
</section>

<section class="portfolio-section">
  <h2>Featured Build Stories</h2>
  <p class="portfolio-section__note">Projects are presented as build stories: problem context, technical implementation, and measurable outcome.</p>
  <div class="case-list">
    <article class="case-item case-item--featured">
      <div class="case-item__meta">
        <span>Benchmarking</span>
        <span>Drift-Aware</span>
        <span>VLDB 2026</span>
      </div>
      <h3 class="case-item__title">DriftBench</h3>
      <div class="case-item__grid">
        <div>
          <p>Built a full-stack drift-aware benchmarking system that helps database researchers generate, reuse, and reproduce evolving datasets and workloads with reproducible pipelines and release automation.</p>
          <p><strong>Stack:</strong> Python, CLI workflows, workload/data generators, CI/CD pipelines, benchmark automation.</p>
          <p class="case-item__links">
            <a class="link-pill" href="https://github.com/Liuguanli/DriftBench">GitHub</a>
            <a class="link-pill link-pill--primary" href="https://pypi.org/project/driftbench-db/"><i class="fab fa-python" aria-hidden="true"></i> PyPI</a>
            <a class="link-pill link-pill--primary" href="https://www.driftbench.com/"><i class="fas fa-globe" aria-hidden="true"></i> Website</a>
            <a class="link-pill" href="https://arxiv.org/abs/2510.10858">VLDB 2026</a>
          </p>
        </div>
        <div class="case-item__media">
          <img src="/images/projects/driftbench-paper.png" alt="DriftBench paper figure">
        </div>
      </div>
    </article>

    <article class="case-item">
      <div class="case-item__meta">
        <span>Benchmarking</span>
        <span>AI-DB</span>
        <span>PostgreSQL Extension</span>
      </div>
      <h3 class="case-item__title">AI-DB Extension Benchmark</h3>
      <p>Built a benchmark and evaluation workflow for AI-DB as a PostgreSQL extension, with recent integration of three core projects: <strong>HMAB</strong>, <strong>GRASP</strong>, and <strong>CoLSE</strong>, enabling unified testing and comparison under one extension-oriented runtime.</p>
      <p><strong>Stack:</strong> PostgreSQL extension workflows, Python automation, reproducible benchmark harnesses, performance analysis.</p>
      <p class="case-item__links">
        <a href="https://github.com/AI-DB-UoM/dbtune">GitHub</a>
      </p>
    </article>

    <article class="case-item">
      <div class="case-item__meta">
        <span>System Design</span>
        <span>Lakehouse</span>
        <span>VLDB 2026 (Submitted)</span>
      </div>
      <h3 class="case-item__title">LayoutPilot / Layout Advisory</h3>
      <div class="case-item__grid">
        <div>
          <p>Designed an advisory backend for analytical data lake workloads, including workload ingestion, SQL parsing, and reusable decision logic for partitioning and intra-file layout choices.</p>
          <p><strong>Stack:</strong> Python, SQL parsing workflows, experiment harnesses, Dockerized service environment.</p>
          <p class="case-item__links"><a href="https://github.com/Liuguanli/layout_advisor">GitHub</a></p>
        </div>
        <div class="case-item__media">
          <img src="/images/projects/layoutpilot-paper.png" alt="LayoutPilot paper figure">
        </div>
      </div>
    </article>

    <article class="case-item">
      <div class="case-item__meta">
        <span>Agent Infrastructure</span>
        <span>Prototype</span>
      </div>
      <h3 class="case-item__title">Metadata-Native Agent Workspace Infrastructure</h3>
      <p>Proposed and prototyped an infrastructure direction where metadata drives task-aware context routing, access control, and recoverable actions for agent workflows.</p>
      <p class="case-item__links">Public write-up and architecture notes will be published in an upcoming portfolio update.</p>
    </article>

    <article class="case-item">
      <div class="case-item__meta">
        <span>LLM + DB</span>
        <span>Applied AI</span>
      </div>
      <h3 class="case-item__title">LLM-Assisted Query Agents</h3>
      <p>Developed agents that translate natural language requests into executable database workflows through retrieval, query decomposition, and result-grounded evaluation.</p>
      <p class="case-item__links">
        <a href="https://github.com/AI-DB-UoM/complex_spatial_data_generation">GitHub</a>
        <a href="https://findanexpert.unimelb.edu.au/scholarlywork/2270718-llm-enhanced-processing-of-complex-spatial-queries?cache=1772143387383">ADC 2025</a>
      </p>
    </article>
  </div>
</section>

<section class="portfolio-section">
  <h2>Selected Publications</h2>
  <p class="portfolio-section__note">This section now reads from structured data and will be connected to the Scholar sync harness in the next workflow steps.</p>
  <div class="publication-list">
    {% assign publications_sorted = site.data.publications | sort: "year" | reverse %}
    {% for pub in publications_sorted %}
    <article class="publication-item">
      <h3 class="publication-item__title">
        {{ pub.title }}
        <span class="publication-badge">{{ pub.status | capitalize }}</span>
      </h3>
      <div class="publication-item__meta">
        {{ pub.authors | join: ", " }}. <strong>{{ pub.venue }}</strong>, {{ pub.year }}.
      </div>
      <div class="publication-item__links">
        {% if pub.pdf_url and pub.pdf_url != "" %}<a href="{{ pub.pdf_url }}">Paper</a>{% endif %}
        {% if pub.arxiv_url and pub.arxiv_url != "" %} <a href="{{ pub.arxiv_url }}">arXiv</a>{% endif %}
        {% if pub.doi_url and pub.doi_url != "" %} <a href="{{ pub.doi_url }}">DOI/Link</a>{% endif %}
        {% if pub.code_url and pub.code_url != "" %} <a href="{{ pub.code_url }}">GitHub</a>{% endif %}
      </div>
    </article>
    {% endfor %}
  </div>
</section>

<section class="portfolio-section build-queue">
  <h2>Build Queue (Next Portfolio Drops)</h2>
  <ul>
    <li><strong>Blockchain Data Platform at nftDb:</strong> Kafka + Airflow ingestion and BigQuery analytics workflow case study.</li>
    <li><strong>Baidu IM Backend:</strong> message protocol and deduplication reliability engineering breakdown.</li>
    <li><strong>Evaluation Tooling:</strong> reusable experiment templates and CI-style benchmark validation pipeline.</li>
  </ul>
</section>

<section class="portfolio-section">
  <h2>Work Experience</h2>
  <div class="timeline">
    {% for exp in site.data.experience %}
    <div class="experience-item">
      <p><strong>{{ exp.start }}-{{ exp.end }}:</strong> {{ exp.role }}, {{ exp.company }} ({{ exp.location }}).</p>
      {% if exp.highlights and exp.highlights.size > 0 %}
      {% for point in exp.highlights %}
      <p>{{ point }}</p>
      {% endfor %}
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>

<section class="portfolio-section">
  <h2>Mentoring, Teaching, and Research Service</h2>
  <div class="teaching-service-card">
    <h3>Mentoring and Supervision</h3>
    <ul>
      {% for item in site.data.teaching_service.mentoring %}
      <li>{{ item }}</li>
      {% endfor %}
    </ul>

    <h3>Teaching</h3>
    <ul>
      {% for t in site.data.teaching_service.teaching %}
      <li><strong>{{ t.course }}</strong>: {{ t.role }} ({{ t.period }}), {{ t.details }}</li>
      {% endfor %}
    </ul>

    <h3>Research Service</h3>
    <ul>
      {% for item in site.data.teaching_service.research_service %}
      <li>{{ item }}</li>
      {% endfor %}
    </ul>
  </div>
</section>
