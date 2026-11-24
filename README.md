# 🌱 AgroFiscal Colombia

### Agricultural Data Engineering & Economic Intelligence Platform

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B?logo=streamlit&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)
![Version](https://img.shields.io/badge/Version-0.1.0-blue)
![Data](https://img.shields.io/badge/Data-Open%20Government-green)

## 📌 Project Overview

**AgroFiscal Colombia** is an agricultural data engineering and economic intelligence project designed to integrate, process, analyze, and visualize public agricultural data in Colombia.

The project focuses on four strategic agricultural sectors:

- 🥔 Potato
- 🌾 Rice
- 🌴 Oil palm
- ☕ Coffee

Its long-term objective is to develop a scalable data platform that combines agricultural production, market prices, economic indicators, and parafiscal revenue information to support data-driven decision-making.

The platform uses official government data sources and aims to make agricultural information more accessible through an interactive public web application.

## 🎯 Project Objectives

- Automate agricultural data extraction from public APIs.
- Build reusable and scalable ETL pipelines.
- Standardize agricultural data from different sources.
- Analyze historical production and productivity trends.
- Integrate updated agricultural information for 2026 and beyond as it becomes available.
- Develop economic and parafiscal revenue indicators.
- Implement predictive analytics and machine learning models.
- Deploy a publicly accessible web application.

## 🌾 Agricultural Sectors

| Sector | Product | Target organization |
|---|---|---|
| Potato | Potato | Fedepapa |
| Rice | Rice | Fedearroz |
| Oil palm | Oil palm | Fedepalma |
| Coffee | Coffee | National Federation of Coffee Growers |

These organizations are potential sources of sector-specific information. This project is independent and is not officially affiliated with them.

## 🚀 Current Features

### Version 0.1.0 — Initial Release

- Direct connection to the Socrata SODA2 API.
- Integration of historical and recent EVA datasets.
- API-level filtering for the four selected agricultural sectors.
- Parallel data extraction and pagination.
- Automatic HTTP retries.
- Data cleaning and column standardization.
- Dynamic detection of available years.
- Interactive agricultural dashboards.
- Geographic analysis by department and municipality.
- Historical production and productivity analysis.
- Exploratory linear trend projections.
- CSV data export.

Live API integration testing for this adapted version is pending.

## 📊 Data Sources

### Currently integrated

| Source | Dataset | Access |
|---|---|---|
| Colombian Open Data Portal | Historical EVA | [Socrata API](https://www.datos.gov.co/resource/2pnw-mmge.json) |
| Colombian Open Data Portal | Recent EVA | [Socrata API](https://www.datos.gov.co/resource/uejq-wxrr.json) |

### Planned integrations

| Source | Information |
|---|---|
| UPRA | Updated agricultural evaluations |
| DANE – SIPSA | Agricultural prices and market supply |
| Fedepapa | Potato sector statistics |
| Fedearroz | Rice sector statistics |
| Fedepalma – SISPA | Oil palm economic indicators |
| National Federation of Coffee Growers | Coffee production and market indicators |
| Ministry of Agriculture | Available public financial information |

Data availability depends on the publication schedule, coverage, and access conditions of each official source.

## 🏗️ System Architecture

### Current architecture

```text
Official Public Data Sources
            |
       Socrata API
            |
   Python Data Extraction
            |
  Data Cleaning & Validation
            |
      Pandas / Cache
            |
    Streamlit Dashboard
            |
      End User
```

### Target architecture

```text
Public APIs / Official Datasets
              |
     Automated ETL Pipelines
              |
       Data Quality Layer
              |
        Google BigQuery
              |
    Raw / Staging / Analytics
              |
     SQL & Business Logic
              |
    Predictive Analytics / ML
              |
   Streamlit / FastAPI / Cloud Run
              |
      Public Web Application
```

The target architecture will be implemented progressively.

## 🛠️ Technology Stack

| Technology | Purpose | Status |
|---|---|---|
| Python | Data processing | Current |
| Pandas | Data transformation | Current |
| NumPy | Numerical analysis | Current |
| Requests | API integration | Current |
| Socrata SODA2 | Data ingestion | Current |
| Streamlit | Web application | Current |
| Plotly | Data visualization | Current |
| BigQuery | Data warehouse | Planned |
| SQL | Analytical modeling | Planned |
| GitHub Actions | Pipeline automation | Planned |
| Scikit-learn | Machine learning | Planned |
| FastAPI | Backend API | Planned |
| Docker | Containerization | Planned |
| Google Cloud Run | Cloud deployment | Planned |

## 📂 Repository Structure

```text
AgroFiscal-Colombia/
│
├── dashboard.py
├── requirements.txt
└── README.md
```

The repository structure will evolve as new modules and data engineering components are implemented.

## ⚙️ Installation and Usage

### Requirements

- Python 3.10 or higher
- Internet connection

### 1. Clone the repository

Clone this repository using the URL available under the GitHub **Code** button.

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the virtual environment

Windows:

```bash
.venv\Scripts\activate
```

Linux or macOS:

```bash
source .venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the application

```bash
python -m streamlit run dashboard.py
```

Open the application in your browser:

```text
http://localhost:8501
```

## 🌐 Public Demo

**Status: Planned**

The application will be deployed to a cloud environment, allowing users to access the agricultural dashboard directly from a web browser without installing Python or cloning the repository.

## 💰 Future Economic and Financial Analytics

A key objective of AgroFiscal Colombia is to build an economic intelligence layer beyond traditional agricultural production dashboards.

Planned indicators include:

- Agricultural market value.
- Historical price variations.
- Potential parafiscal revenue.
- Actual parafiscal revenue, subject to public data availability.
- Revenue gaps.
- Budget execution.
- Regional economic performance.
- Financial anomaly detection.
- Production and price forecasting.

Estimated revenue will be clearly distinguished from officially reported revenue.

## 🗺️ Development Roadmap

### Phase 1 — Agricultural Data Foundation

- [x] Initial Socrata API connector implementation.
- [x] Historical agricultural dataset integration.
- [x] Four-sector filtering implementation.
- [x] Initial Streamlit dashboard.
- [ ] Validate live API queries and crop coverage.
- [ ] Integrate available 2026 agricultural records.

### Phase 2 — Data Engineering

- [ ] Modular ETL architecture.
- [ ] Automated incremental data ingestion.
- [ ] Data quality tests.
- [ ] BigQuery data warehouse.
- [ ] Dimensional data modeling.
- [ ] GitHub Actions automation.

### Phase 3 — Economic Intelligence

- [ ] Agricultural market price integration.
- [ ] Sector-specific data connectors.
- [ ] Parafiscal regulation and rate catalog.
- [ ] Potential revenue estimation.
- [ ] Public financial data integration.
- [ ] Revenue gap analysis.

### Phase 4 — Artificial Intelligence

- [ ] Time-series forecasting.
- [ ] Model validation and performance evaluation.
- [ ] Anomaly detection.
- [ ] Economic risk indicators.

### Phase 5 — Cloud Deployment

- [ ] Public Streamlit application.
- [ ] Docker containerization.
- [ ] FastAPI integration.
- [ ] Google Cloud Run deployment.
- [ ] Application monitoring.

## ⚠️ Data Limitations

- Official agricultural data may be published with a time lag.
- Complete municipal-level production data for 2026 has not yet been verified.
- Detailed parafiscal transactions may not be publicly available.
- Forecasts and estimates must not be interpreted as official government figures.
- This project is currently under active development.

## 🤝 Acknowledgments

The initial data extraction and visualization components are adapted from the [AgroColombia project](https://github.com/trabajocientifico/AgroColombia), developed by the Trabajo Científico team and collaborating organizations.

AgroFiscal Colombia extends this foundation toward specialized agricultural data engineering, economic intelligence, financial analytics, and cloud deployment.

Credit for the original implementation remains with its respective authors.

## 📄 License

The upstream AgroColombia README identifies its project license as MIT. The original license text and copyright notices must be verified and preserved before redistribution.

Public datasets remain subject to their respective terms of use.

## 👩‍💻 About the Project

This project is part of a professional portfolio focused on:

- Data Engineering
- Data Analytics
- Business Intelligence
- Cloud Computing
- Artificial Intelligence
- Open Data

The goal is to combine these disciplines to develop practical, scalable, and transparent data solutions for Colombia's agricultural sector.

---

**AgroFiscal Colombia — From Agricultural Data to Economic Intelligence.**

🚧 Work in progress | Initial Release v0.1.0

