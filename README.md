<div align="center">
  <h1>
    <strong>Hi, I'm Denis 👋</strong>
    <img src="assets/images/wave.gif" width="30" alt="wave">
  </h1>

  <p>
    <b>Backend Engineer</b> · Python / FastAPI · Distributed Systems & Production-Ready APIs
  </p>

  <p>
    <em>
      <a href="https://github.com/wittiden">
        <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=200&size=14&pause=1000&color=FFFFFF&center=true&vCenter=true&width=560&lines=Backend+Engineer;Building+Scalable+APIs+%26+Distributed+Systems;Python+%7C+FastAPI+%7C+REST+%26+GraphQL;System+Design" alt="Typing SVG"/>
      </a>
    </em>
  </p>

</div>

---

## Featured Projects

### 📋 [TaskService](https://github.com/wittiden/TaskService)

Production-ready task management REST API showcasing **Clean Architecture** and a full observability stack.

* JWT auth with RSA-signed access/refresh tokens and rotation; RBAC (Admin / VIP / Standard)
* Task CRUD with status tracking and audit logging; per-endpoint rate limiting, Redis caching
* **Clean Architecture** end-to-end, wired with the **Dishka** DI container
* **Full MELT observability**: Prometheus, Grafana, Sentry, structured Loguru logging
* CI/CD on GitHub Actions: Ruff, Pyright, matrix tests (Python 3.12–3.14) with real Postgres/Redis, coverage gating (≥70%) → Codecov
* Docker Compose with optional profiles for PgAdmin, RedisInsight, Grafana

**Stack:** FastAPI · SQLAlchemy 2.0 (async) · PostgreSQL · Redis · Alembic · Dishka · Pytest · Testcontainers · uv

---

### 💳 [DigitalBank](https://github.com/wittiden/DigitalBank)

Digital banking REST API modeling real financial operations with the data integrity a banking system needs.

* RSA-signed JWT (RS256) with access/refresh rotation and token revocation
* Debit/credit wallets with hashed PIN, block/unblock, soft-close; multi-currency balances
* Deposits, withdrawals, transfers with fee calculation; full transaction history with status tracking
* Admin surface for users, wallets, balances, transactions
* Atomic financial operations via async **Unit of Work**; consistent modular layout (`api` → `contracts` → `service` → `repository`)

**Stack:** FastAPI · SQLAlchemy 2.0 (async) · PostgreSQL · Alembic · Dishka · PyJWT (RSA) · Pydantic v2

---

### 🌱 DAOS — Digital Agro Optimization System *(private / competition project)*

Backend platform for agricultural production optimization, built as part of a competition track. Source is kept private.

* Dual API surface: **REST** (FastAPI) for CRUD/integrations and **GraphQL** (Strawberry) for flexible client-driven queries over related entities
* **PostgreSQL + MongoDB split**: PostgreSQL for transactional/relational domain data (with Alembic migrations and async SQLAlchemy 2.0), MongoDB for scenario-based documents — flexible, schema-less scenario definitions and calculation inputs that don't fit the relational model
* **Pyomo + GLPK** optimization engine with a dedicated DTO layer
* Keycloak auth (realm roles `free` / `standard` / `ultima` / `admin`) shared by both API contours
* Celery + RabbitMQ background jobs, Redis for rate limiting/cache/results, SQLAdmin admin surface

**Stack:** FastAPI · Strawberry GraphQL · SQLAlchemy 2.0 (async) · PostgreSQL · MongoDB · Alembic · Keycloak · Redis · RabbitMQ · Celery · Pyomo / GLPK · Dishka · SQLAdmin · uv

> Status: private repository. Architecture walkthrough available on request.

---

## 🛠 Tech Stack

<h5>⚙️ Backend Core</h5>
<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Strawberry_GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white"/>
<img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white"/>
<img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white"/>
<img src="https://img.shields.io/badge/Dishka-DI%20Container-7c3aed?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Pyomo-4B8BBE?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SQLAdmin-D71F00?style=for-the-badge"/>
<img src="https://img.shields.io/badge/HTTPX-5A29E4?style=for-the-badge"/>
</p>

<h5>🗄️ Data & Storage</h5>
<p>
<img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Alembic-4B8BBE?style=for-the-badge"/>
</p>

<h5>🔐 Security</h5>
<p>
<img src="https://img.shields.io/badge/PyJWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white"/>
<img src="https://img.shields.io/badge/Keycloak-4D4D4D?style=for-the-badge&logo=keycloak&logoColor=white"/>
<img src="https://img.shields.io/badge/SlowAPI-FF6B6B?style=for-the-badge"/>
</p>

<h5>🧪 Testing</h5>
<p>
<img src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white"/>
<img src="https://img.shields.io/badge/Testcontainers-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/factory--boy-4C1?style=for-the-badge"/>
</p>

<h5>🔄 Build & Quality</h5>
<p>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=uv&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/Codecov-F01F7A?style=for-the-badge&logo=codecov&logoColor=white"/>
<img src="https://img.shields.io/badge/Ruff-2D3748?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Pyright-0078D4?style=for-the-badge"/>
<img src="https://img.shields.io/badge/pre--commit-FAB040?style=for-the-badge"/>
</p>

<h5>📊 Observability</h5>
<p>
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/Loki-FCC624?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Promtail-FFA500?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white"/>
<img src="https://img.shields.io/badge/Loguru-1F1F1F?style=for-the-badge"/>
</p>

---

## 🧰 Tools

<p align="center">
  <img src="https://skillicons.dev/icons?i=github,gitlab,pycharm,git,linux,obsidian" />
</p>

---

<p align="center">
  <sub>Open to backend roles where reliability and clean architecture are part of the job, not an afterthought.</sub>
</p>
