# ReNova Connect — Transform API

**Transform API** is the core service of the **ReNova Connect** system, providing a unified interface to clinic data.
It integrates and exposes data collected from Clinicia for both Telegram and WhatsApp bots.

---

## 🚀 Features

- REST API for Telegram and WhatsApp bots  
- Works with PostgreSQL and Redis  
- Real-time data updates and caching  
- Authentication and logging  
- Fully asynchronous (FastAPI + asyncio)

---

## 🧩 Technologies

| Component | Technology |
|------------|-------------|
| Framework | FastAPI |
| ORM | SQLAlchemy / asyncpg |
| Cache | Redis |
| Database | PostgreSQL |
| Auth | JWT (optional) |
| Logging | loguru |
| Deploy | Docker / Docker Compose |

---

## ⚙️ Run locally

```bash
cp .env.example .env
docker-compose up --build
```

Docs: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 📦 Structure

```
app/
 ├── api/              # FastAPI endpoints
 ├── services/         # Business logic
 ├── models/           # ORM models
 ├── core/             # Config & middlewares
 └── main.py           # Entry point
```

---

## 🧠 Architecture

```
Clinicia → Collector → PostgreSQL/Redis → Transform API → Telegram/WhatsApp Bots
```

---

## 🧰 Environment Variables

| Variable | Description |
|-----------|-------------|
| `DATABASE_URL` | PostgreSQL connection string |
| `REDIS_URL` | Redis connection string |
| `API_TOKEN` | Access token for bots |

---

## 🧾 License
MIT License  
© ReNova Beauty Hub
