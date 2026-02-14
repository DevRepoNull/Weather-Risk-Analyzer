# Weather-Risk-Analyzer

## 1. Vision
We are building a Weather Risk Analyzer platform that transforms raw weather data into actionable risk insights such as:

- Freeze Risk (Pipe Damage Risk)
- Heat Risk (Health-Oriented Index)
- Future: Agriculture Risk

The goal is to design a modular, production-ready system combining .NET backend architecture with Python-based Machine Learning services.

This project is designed as a portfolio-grade system demonstrating:

- Clean Architecture
- Microservice Communication
- Time Series Forecasting
- Risk Scoring Engine
- CI/CD and Containerization
- Team Engineering Practices

## 2.Core Problem Statement
Raw weather data is available publicly, but decision-oriented risk interpretation is not easily accessible.

We aim to build a system that:

1. Collects historical and live weather data
2. Predicts short-term weather conditions
3. Calculates domain-specific risk scores
4. Exposes results via API and dashboard

## 3. High-Level Architecture
System Components:

1. Data Collector Service (Python)
- Fetches historical data from public sources such as Meteostat
- Stores structured data in database

2. ML Forecast Service (Python + FastAPI)
- Trains time-series model
- Provides prediction endpoint

3. Weather Risk API (.NET 8, ASP.NET Core)
- Clean Architecture
- CQRS
- Database access
- Risk Engine module
- Calls ML service

4. Dashboard (Phase 2)
- Risk visualization
- Forecast charts

## 4. Tech Stack (Initial)

#### Backend:
- .NET 8
- ASP.NET Core Web API
- EF Core
- PostgreSQL

#### ML:
- Python
- FastAPI
- Pandas
- scikit-learn (initial phase)


#### Infrastructure:
- Docker
- GitHub Actions (later phase)

## 5. Engineering Rules

1. No direct commits to main branch

2. All features via Pull Request

3. Each PR must:
- Reference an Issue
- Include short technical description

4. Commit messages must follow clear format:
    type(scope): short description
    Example:
    feat(api): add temperature forecast endpoint

5. Every architectural decision must be documented in /docs as ADR.

## 6. Repository Structure

weather-risk-analyzer/
- README.md
- docs/
    - project-charter.md
    - architecture.md
    - adr/
- src/
    - backend/
    - ml-service/
- docker/
- .github/
    - workflows/

## 7. Milestone Plan

Milestone 1 — Foundation (Week 1–2)
- Repository setup
- Architecture diagram
- Data source validation
- Data ingestion prototype

Milestone 2 — Forecasting (Week 3–4)
- Time series model
- Prediction endpoint
- Backend integration

Milestone 3 — Risk Engine (Week 5–6)
- Freeze Risk module
- Heat Risk module
- Confidence interval output

Milestone 4 — Deployment (Week 7+)
- Dockerization
- CI/CD
- Public demo

## 8. Definition of Done (Per Feature)

A feature is considered complete only if:

- Code implemented
- Unit tests added
- Documentation updated
- PR reviewed and approved
- No unresolved warnings