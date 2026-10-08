<div align="center">
  <img src="assets/brand-header.svg" width="100%" alt="SUNTZZ // Engineering, Data &amp; Systems" />
</div>

<br/>

## Executive Overview

**Systems Engineering student and Data Analyst** based in Bogotá, Colombia. My work focuses on building reproducible machine learning pipelines, decoupled mobile architectures with accessibility in mind, and typed backend microservices.

Me enfoco en el desarrollo de software y análisis de datos guiado por rigor metodológico: evaluación empírica con particiones congeladas, pruebas automatizadas y arquitecturas modulares donde cada componente tiene una responsabilidad delimitada.

---

## Technical Capabilities

| Domain | Core Competencies | Tooling & Frameworks |
| :--- | :--- | :--- |
| **Applied Machine Learning &amp; Data** | Experimental design, ensemble modeling, ablation studies, probabilistic calibration, leakage auditing. | `Python`, `TensorFlow / Keras`, `scikit-learn`, `pandas`, `NumPy`, `Joblib` |
| **Mobile &amp; Accessibility** | Clean Architecture, decoupled domain services, voice-assisted interfaces, geospatial calculations. | `React Native`, `Expo`, `TypeScript`, `Expo Speech`, `React Navigation` |
| **Backend &amp; APIs** | RESTful routing, asynchronous execution, typed data contracts, automated integration tests. | `FastAPI`, `Uvicorn`, `HTTPX`, `Starlette TestClient` |
| **Engineering Discipline** | Test-driven development (TDD), CI workflows, strict type checking, reproducible artifact tracking. | `Pytest`, `Jest`, `Git`, `GitHub Actions`, `Linux / macOS` |

---

## Selected Engineering Cases

### 01 / Deep Neural Ensemble for Credit Risk Evaluation
**Repository:** [`suntzz/riesgo-crediticio`](https://github.com/suntzz/riesgo-crediticio)  
**Scope:** Machine Learning • Supervised Classification • Empirical Model Selection

An end-to-end predictive modeling system designed to classify financial credit risk under severe asymmetry between false approvals (default risk) and false rejections (commercial opportunity cost).

* **Dataset & Partitioning:** 49,650 verified financial observations processed into 44 features. Partitioned with frozen stratified splits (70% Train: 34,755 | 15% Validation: 7,447 | 15% Test: 7,448).
* **Experimental Rigor:** Conducted 74 structured experiments across 3 phases (baseline optimization, $L_2$ regularization, multi-seed exploration, and diverse architectural ensembles).
* **Final Evaluated Architecture (`Ensemble_Top3_Diverso`):** Heterogeneous linear combination of three Keras networks ($12,995$ total trainable parameters):
  * Model 1: Dense [64, 32, 16] (ReLU, Dropout 0.15)
  * Model 2: Dense [32, 16] (LeakyReLU $\alpha=0.1$, Dropout 0.15)
  * Model 3: Dense [64, 32, 16] (ReLU, Dropout 0.20, seed 2026)
* **Audited Evaluation on Frozen Test Set (7,448 observations):**
  * **Test ROC-AUC:** `0.74482` (vs. Validation ROC-AUC `0.75382`, demonstrating $-1.19\%$ delta and zero data leakage).
  * **Test PR-AUC:** `0.73512` | **Test Log Loss:** `0.5963` | **Test Brier Score:** `0.2050`
  * **Test Accuracy:** `67.48%` | **Test F1-Score:** `0.6715`
  * **Test Confusion Matrix:** True Negatives: $2,550$ | False Positives: $1,174$ | False Negatives: $1,248$ | True Positives: $2,476$.

---

### 02 / TransmiGuía — Voice-Assisted Urban Transit Navigation
**Repository:** [`suntzz/transmiguia`](https://github.com/suntzz/transmiguia)  
**Scope:** Mobile Architecture • Spatial Computing • Accessibility Engineering

An accessible urban transit navigation assistant engineered for Bogotá's TransMilenio mass transit system. Designed to assist users through multimodal voice synthesis, haptic notifications, and step-by-step contextual guidance.

* **Architecture & Clean Code:** Refactored from a monolithic codebase into a 5-tier Clean Architecture (Domain Models, Domain Rules, Text Matching Core, Geospatial Engine, Application Screens).
* **Verified Implementation:**
  * Polymorphic Haversine geospatial calculation (`src/core/geo/distance.ts`) for real-time station proximity.
  * Lexical normalization and fuzzy station matching (`src/core/text/stationMatcher.ts`).
  * Speech synthesis orchestration (`expo-speech`) and custom tactile alerts (`expo-haptics`).
  * Automated testing suite: **28 of 28 unit tests passing** with strict TypeScript type-checking (`0 errors, 0 warnings`).
* **Operational Scope (Demo Mode):** Implements a dedicated simulation engine (`demoService.ts`) enabling full field verification across the 6 journey stages (destination select, walking guide, station arrival, boarding, transfers, destination arrival) without requiring live municipal fleet telemetry.

---

### 03 / SmartBuilding API — Residential Administration Microservice
**Repository:** [`suntzz/smartbuilding-api`](https://github.com/suntzz/smartbuilding-api)  
**Scope:** Backend Engineering • RESTful API Design • Integration Testing

A lightweight, typed REST API prototype built with FastAPI for resident directory querying and property administrative management.

* **Endpoints Implemented:**
  * `GET /`: Health check and service entry point.
  * `GET /residentes`: Full directory listing of registered residents.
  * `GET /residentes/{residente_id}`: Parameterized single-record retrieval by primary identifier.
* **Architecture & Testing:** Asynchronous request handling with Uvicorn and automated test coverage via `pytest` and Starlette `TestClient` (`tests/test_residentes.py`).

---

### 04 / Academic Evaluation & Cohort Metrics Engine
**Repository:** [`suntzz/gestor_calificaciones`](https://github.com/suntzz/gestor_calificaciones)  
**Scope:** Defensive Programming • Algorithmic Logic • Test-Driven Development

A pure Python module for calculating individual academic summaries and cohort statistics with strict defensive boundaries.

* **Verified Logic:** Score validation within strict range $[0.0, 5.0]$, empty collection guardrails with custom `ValueError` exceptions, student entity mapping, and cohort summary generation.
* **Deterministic Tie-Breaking:** Explicit collision handling raising exceptions when multiple students share the highest GPA, preventing ambiguous ranking.
* **Test Suite:** Comprehensive unit test coverage using `pytest` validating boundary conditions, extreme scores, and nominal cohort distributions.

---

## Technical Dossier & Activity

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="profile-3d-contrib/profile-night-view.svg">
    <source media="(prefers-color-scheme: light)" srcset="profile-3d-contrib/profile-green-animate.svg">
    <img src="profile-3d-contrib/profile-night-view.svg" width="100%" alt="3D Isometric Contribution Skyline" />
  </picture>
</div>

<br/>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/suntzz/suntzz/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/suntzz/suntzz/output/github-contribution-grid-snake.svg">
    <img alt="Contribution Grid Snake" src="https://raw.githubusercontent.com/suntzz/suntzz/output/github-contribution-grid-snake-dark.svg" width="100%" />
  </picture>
</div>

---

## Contact & Professional Channels

* **Location:** Bogotá, Colombia
* **Direct Email:** [`solanoivan295@gmail.com`](mailto:solanoivan295@gmail.com)
* **GitHub:** [`github.com/suntzz`](https://github.com/suntzz)

<br/>

<div align="center">
  <sub>SUNTZZ TECHNICAL DOSSIER // REPRODUCIBLE SYSTEMS // BUILT WITH SYSTEM DISCIPLINE</sub>
</div>
