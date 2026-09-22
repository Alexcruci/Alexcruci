# Hi, I'm Alex 👋

### Junior Data Engineer | Python · SQL · PostgreSQL · Docker · Azure

I'm a Junior Data Engineer based in Italy, focused on building data pipelines, relational databases, and practical analytics projects.

I enjoy working with data throughout its lifecycle: collecting it from real-world sources, understanding its limitations, transforming it into a consistent model, and making it useful for analysis.

I recently completed **Project Zero**, an end-to-end job-market data pipeline with reproducible Docker execution and a validated deployment on Microsoft Azure.

I'm currently looking for opportunities as a **Junior Data Engineer**, **Junior ETL Developer**, **BI/Data Engineer**, or data-focused developer.

---

## 🛠️ Tech Stack

### Data Engineering

- **Python**, **SQL**, **Pandas**
- **PostgreSQL** and relational data modeling
- REST API ingestion, pagination, and retry handling
- ETL pipelines and ELT concepts
- Data cleaning, transformation, and validation
- JSON and source-data preservation
- Transactional database loading

### Containers & Cloud

Practical experience gained through Project Zero:

- **Docker** — containerized Python ETL
- **Docker Compose** — local ETL and PostgreSQL orchestration
- **Azure Container Registry** — Docker image storage and distribution
- **Azure Container Apps Jobs** — manually triggered cloud execution
- **Azure Database for PostgreSQL** — managed relational storage
- Managed identities, registry permissions, and runtime secrets

### Analytics & Visualization

- **Power BI**
- SQL profiling and analytical queries
- Exploratory data analysis
- KPI development
- Validation of dashboard results against database queries

### Development Tools

- **Git & GitHub**
- Linux and Windows
- Python virtual environments
- Environment-based configuration
- MySQL

### Continuing to Develop

- Automated testing for data pipelines
- Cloud deployment and operational practices
- Data warehousing and incremental processing
- Monitoring and observability

---

## 🚀 Projects

### 🔹 Project Zero — IT Job Market Data Pipeline

**Completed: local ETL, analytics, Docker, and Azure deployment**

An end-to-end Data Engineering project that collects technology job postings relevant to the Italian market from **Adzuna and FreeHire**, transforms heterogeneous API responses into a shared schema, and loads the results into PostgreSQL for SQL analysis and Power BI reporting.

[**Explore the repository →**](https://github.com/Alexcruci/it-job-market-analytics)

#### End-to-End Workflow

```text
Adzuna + FreeHire APIs
          ↓
    Python extraction
          ↓
       Raw JSON
          ↓
Transformation & validation
          ↓
    PostgreSQL database
          ↓
 SQL analysis → Power BI
```

The pipeline runs locally through **Docker Compose** or in Azure through a **Container Apps Job** using an image published to **Azure Container Registry**.

The cloud execution initializes the schema and runs the ETL against **Azure Database for PostgreSQL**, without importing a local database dump.

#### What I Built

- API extraction with pagination, timeouts, and retries
- Raw JSON preservation for debugging and transformation reruns
- Source-specific transformation into a common schema
- Within-source deduplication and required-field validation
- Conservative filtering of identified non-job records
- City normalization and explicit handling of missing data
- A relational model with `jobs`, `skills`, and `job_skills`
- Transactional full-refresh loading
- SQL profiling and analysis
- A two-page Power BI report
- Containerized execution with database persistence and health checks
- Repeatable schema initialization for cloud execution
- Azure deployment with managed-identity image pulls and runtime secrets

#### Verified Results

The final Azure execution populated:

| Metric | Result |
| --- | ---: |
| Job postings | 12,718 |
| Adzuna postings | 2,718 |
| FreeHire postings | 10,000 |
| Unique skills | 775 |
| Job–skill relationships | 86,395 |

These figures describe one validated run. Counts vary because the pipeline consumes live APIs. The Power BI report and published analytical findings use the earlier Version 1 snapshot.

#### Engineering Lessons

The project gave me practical experience with problems beyond writing the initial ETL:

- **Data quality:** SQL profiling exposed non-job records; dashboard validation revealed city-normalization inconsistencies. Both were addressed upstream.
- **Failure handling:** retries manage selected temporary API errors, while failed extraction stops downstream processing.
- **Reproducibility:** the Docker workflow was validated from a fresh clone without an existing project database or Python environment.
- **Cloud debugging:** deployment required resolving region restrictions, resource-provider registration, registry permissions, and database connectivity.
- **Deployment validation:** a Job initially reported success while using an outdated image. Inspecting the published image and checking database contents revealed the problem.

The scope is deliberately bounded: execution is manual, loading uses a full refresh, and cross-source entity resolution, historical snapshots, and an automated test suite are not implemented. The dataset is a collected sample, not a representative measure of the entire Italian technology job market.

**Stack:**  
`Python` · `Pandas` · `REST APIs` · `PostgreSQL` · `SQL` · `Power BI` · `Docker` · `Docker Compose` · `Microsoft Azure`

---

### 🎮 Indie Games Database — In Development

A data engineering project inspired by platforms such as VNDB, focused on cataloguing smaller and niche independent games.

The first version is planned to run locally, with an emphasis on **data architecture and ingestion**.

Planned scope:

- Data ingestion from multiple sources
- PostgreSQL relational database
- Game, developer, engine, and genre entities
- Tagging and development-status tracking
- Data normalization and deduplication
- ETL pipelines
- A simple web interface or API

**Planned stack:**  
`Python` · `PostgreSQL` · `SQL` · `ETL` · `FastAPI / Flask`

---

### 🌐 Project Discovery — Research & Product Design

A long-term exploration of a social discovery platform that connects people through shared interests.

The project is in **Phase 0: research and product design**, before implementation.

Current focus:

- Product requirements and competitive analysis
- Data model exploration
- User discovery and early validation
- Feature design
- Technical architecture planning

Potential implementation areas include backend services, databases, APIs, and recommendation or discovery systems.

---

## 📚 Background

I completed an intensive **Junior Data Engineer training program of approximately 500 hours**, covering:

- Python, SQL, and Pandas
- Relational databases and NoSQL
- ETL pipelines and data modeling
- Power BI
- AWS fundamentals

I also have previous experience with IT systems and a background in web technologies and UI/UX.

My personal projects help me turn that foundation into practical experience with designing, implementing, debugging, and explaining complete data workflows.

---

## 🎯 What I'm Looking For

I'm interested in junior roles involving:

- Data pipelines and ETL / ELT
- Python, SQL, and PostgreSQL
- Relational data modeling
- Cloud data platforms
- Data warehouses
- Business Intelligence

I'm particularly interested in teams where I can contribute to real data systems, receive thoughtful code review, and learn from experienced Data Engineers.

---

## 📫 Contact

- **LinkedIn:** [Alex Cruceru](https://www.linkedin.com/in/alexcruci/)
- **Email:** [cruceru_alex@hotmail.it](mailto:cruceru_alex@hotmail.it)
- **GitHub:** [Alexcruci](https://github.com/Alexcruci)
