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

## 🌟 About Me

I'm a backend engineer focused on **scalable APIs**, **distributed systems**, and **production-ready backend services**. I like building systems that stay predictable under load: clear service boundaries, async I/O done right, and enough observability that a 3 a.m. incident is a quick lookup instead of a guessing game.

I care about systems that are:

- **Scalable** — designed to handle growth without a rewrite
- **Maintainable** — clean architecture, explicit contracts, readable code
- **Fault-tolerant** — graceful degradation instead of cascading failure
- **Observable** — metrics, structured logs, and traces that actually help during an incident
- **Easy to extend** — new features shouldn't require fighting the existing design

My day-to-day interests: backend architecture, asynchronous processing, database performance, testing, CI/CD, and full-stack observability (the MELT stack: Metrics, Events, Logs, Traces).

---

## 🎯 Engineering Goal

Build reliable backend systems capable of handling real production traffic with high availability, efficient resource usage, and observability built in from day one — not bolted on after the first outage.

---

## 🚀 Featured Projects

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

<h5>🔐 Security & Validation</h5>
<p>
<img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white"/>
<img src="https://img.shields.io/badge/PyJWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white"/>
<img src="https://img.shields.io/badge/bcrypt-5A3E2B?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SlowAPI-FF6B6B?style=for-the-badge"/>
</p>

<h5>🚀 Deployment</h5>
<p>
<img src="https://img.shields.io/badge/Uvicorn-499848?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Gunicorn-499848?style=for-the-badge&logo=gunicorn&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
</p>

<h5>🧪 Testing</h5>
<p>
<img src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white"/>
<img src="https://img.shields.io/badge/HTTPX-5A29E4?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Testcontainers-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Faker-FF6B6B?style=for-the-badge"/>
<img src="https://img.shields.io/badge/factory--boy-4C1?style=for-the-badge"/>
</p>

<h5>🔄 CI/CD & Code Quality</h5>
<p>
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
  <img src="https://skillicons.dev/icons?i=github,pycharm,git,linux" />
</p>

---

## 📈 GitHub Activity

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=wittiden&bg_color=0d1117&color=009688&line=009688&point=ffffff&area=true&hide_border=true"/>
</p>

---

<p align="center">
  <sub>Open to backend roles where reliability and clean architecture are part of the job, not an afterthought.</sub>
</p>
