# Mooketsi Magwaza

Full-stack developer. I like taking a product from "just an idea" to a
system that actually runs — real auth, a real database, a real deploy
story — not just a UI over an API someone else designed. Most of what's
below is still actively evolving; I ship in public and keep iterating.

📫 **[mooketsimagwazajr@gmail.com](mailto:mooketsimagwazajr@gmail.com)** —
open to backend, frontend or full-stack roles, entry-to-intermediate level.

---

## Featured Work

### 🔗 [StockLink](https://github.com/MVMC4/stocklink)

A B2B marketplace connecting warehouses to retail stores: warehouses
publish server-priced stock by unit, case and pallet; stores order across
every connected warehouse from one cart; compatible demand pools
automatically into consolidated bulk orders; every listing carries photos
stores can browse before they buy.

- Four independent Rust/Axum services (identity, commerce, notifications,
  media), each with its own PostgreSQL database, behind one nginx gateway
- Stateless JWT auth verified independently by every service, a
  Redis-backed denylist and rate limiter, internal-only service-to-service
  APIs that never touch the public gateway
- React/Vite/TypeScript frontend with a hand-built design system — no
  component library, every pixel is a deliberate choice
- Docker Compose for local dev, health-gated zero-downtime rolling updates,
  a generated docs site from the repo's own Markdown
- **Stack:** Rust · Axum · sqlx · PostgreSQL · Redis · React · TypeScript · Docker

### 🔗 [Transit Route Optimization](https://github.com/MVMC4/transit-route-optimization)

A full-stack transit platform: a route-optimization API, an operations
dashboard, a rider-facing app, a public marketing site, and real developer
documentation (Fumadocs) with sign-up and API access gated behind proper
auth — five independent apps that all have to agree with each other.

- Node.js/TypeScript API with route CRUD and an optimization endpoint,
  backed by PostgreSQL
- Session-based auth gating the docs and dashboard, verified server-side on
  every protected request rather than trusting a cookie's mere presence
- Five deployable apps (api, admin, rider, marketing, docs) behind one
  Docker Compose stack
- **Stack:** TypeScript · Node.js · PostgreSQL · Docker

---

## Tech Stack

**Backend**
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-000000?style=for-the-badge&logo=rust&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)

**Frontend**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)

**Data**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

**Ops**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

---

## Other Projects

A few smaller, finished things — mostly built because I wanted the tool to
exist, not as a portfolio exercise:

| Project | What it is |
| --- | --- |
| [GlassHID](https://github.com/MVMC4/GlassHID) | Turns an Android phone into an offline Bluetooth keyboard/trackpad/remote/gamepad |
| [obsidian-excalidraw-low-latency](https://github.com/MVMC4/obsidian-excalidraw-low-latency) | Low-latency pen companion plugin for Obsidian Excalidraw |
| [obsidian-blackboard](https://github.com/MVMC4/obsidian-blackboard) | Handwritten drawings in Obsidian Canvas |
| [obsidian-sync-ios](https://github.com/MVMC4/obsidian-sync-ios) | Free, open-source iOS companion for Obsidian + Syncthing |
| [team-watch](https://github.com/MVMC4/team-watch) | Data visualization tool for scraped hackathon data |

---

*If you're reading this as part of a hiring process: thanks for going this
deep. Happy to walk through any of the above — architecture decisions,
what I'd do differently now, all of it.*
