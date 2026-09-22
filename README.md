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
        <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=200&size=14&pause=1000&color=FFFFFF&center=true&vCenter=true&width=560&lines=Backend+Engineer;Building+Scalable+APIs+%26+Distributed+Systems;Python+%7C+FastAPI+%7C+System+Design" alt="Typing SVG"/>
      </a>
    </em>
  </p>
  
</div>

---

## Featured Projects

### 📋 [TaskService](https://github.com/wittiden/TaskService)

A production-ready task management REST API built to showcase a full **Clean Architecture** implementation with a complete observability stack, not just CRUD endpoints.

**What it does:**
- JWT authentication with RSA-signed access/refresh tokens and full token rotation
- Role-based access control (Admin / VIP / Standard)
- Task CRUD with status tracking (active, completed, closed) and full audit logging
- Per-endpoint rate limiting and Redis-backed session/user caching

**What makes it interesting:**
- **Clean Architecture** end-to-end — presentation, application, domain, and infrastructure layers stay properly decoupled, wired together with the **Dishka** DI container
- **Full MELT observability**: Prometheus metrics, Grafana dashboards, Sentry error tracking, and structured Loguru logging with rotation and JSON output for log aggregation
- **CI/CD pipeline** on GitHub Actions running lint (Ruff), type checking (Pyright), and a matrix test suite across Python 3.12–3.14 with real Postgres and Redis service containers, plus coverage gating (≥70%) uploaded to Codecov
- Fully containerized with Docker Compose, including optional profiles for PgAdmin, RedisInsight, and Grafana

**Stack:** FastAPI · SQLAlchemy 2.0 (async) · PostgreSQL · Redis · Alembic · Dishka · Pytest · Testcontainers

---

### 💳 [DigitalBank](https://github.com/wittiden/DigitalBank)

A digital banking REST API modeling real financial operations — multi-currency wallets, balances, and transfers — with the kind of data integrity and access control a banking system actually needs.

**What it does:**
- RSA-signed JWT auth (RS256) with access/refresh rotation and token revocation
- Debit and credit wallets protected by a hashed PIN, with block/unblock and soft-close flows
- Multi-currency balances (regular and foreign) per wallet, with admin freeze/unfreeze controls
- Deposits, withdrawals, and inter-wallet transfers with fee calculation
- Full transaction history with status tracking (pending / success / failed) and type classification
- Dedicated admin surface for managing users, wallets, balances, and transactions

**What makes it interesting:**
- **Domain modeling that mirrors real banking constraints**: `User → Wallet → Balance → Transaction`, where every financial operation is atomic and auditable
- Consistent modular layout per feature (`api` → `contracts` → `service` → `repository`) so every module is easy to navigate the same way
- Async **Unit of Work** pattern around every session/commit boundary — no partial writes on financial operations
- Deployed via Docker Compose with a dedicated migrations profile, keeping schema changes explicit and repeatable

**Stack:** FastAPI · SQLAlchemy 2.0 (async) · PostgreSQL · Alembic · Dishka · PyJWT (RSA) · Pydantic v2

---

## 🛠 Tech Stack

<h5>⚙️ Backend Core</h5>
<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white"/>
<img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white"/>
<img src="https://img.shields.io/badge/Dishka-DI%20Container-7c3aed?style=for-the-badge"/>
</p>

<h5>🗄️ Data & Storage</h5>
<p>
<img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
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
<img src="https://img.shields.io/badge/HTTPX-5A29E4?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Testcontainers-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/factory--boy-4C1?style=for-the-badge"/>
</p>

<h5>🔄 Build & Quality</h5>
<p>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
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
  <img src="https://skillicons.dev/icons?i=github,pycharm,git,linux,obsidian" />
</p>

---

<p align="center">
  <sub>Open to backend roles where reliability and clean architecture are part of the job, not an afterthought.</sub>
</p>
