# Hi there, I'm **Mooketsi Magwaza** 👋

### Full-Stack Software Developer | Rust • TypeScript • Node.js • PostgreSQL

I build full systems, not just screens — backend services, the APIs in front of
them, and the UI on top, usually running behind Docker Compose with real
auth, migrations and observability from the start. The two projects below
are the current, actively-developed proof of that.

---

## Featured Work

### 🔗 [StockLink](https://github.com/MVMC4/stocklink)

A B2B marketplace connecting warehouses to retail stores: warehouses publish
server-priced stock by unit, case and pallet; stores order across every
connected warehouse from one cart; compatible demand pools automatically
into consolidated bulk orders; every shipment is tracked to the door.

- **Backend:** four independent Rust/Axum services (identity, commerce,
  notifications, media), each with its own PostgreSQL database, behind one
  nginx gateway — split by domain, not by table
- **Auth:** stateless JWT verified independently by every service, a
  Redis-backed denylist/rate-limiter, internal-only service-to-service APIs
- **Frontend:** React, Vite, TypeScript, TanStack Query — a hand-built
  design system (no component library)
- **Ops:** Docker Compose for local dev, health-gated zero-downtime rolling
  updates, Prometheus/Grafana observability, a generated docs site
- **Stack:** Rust · Axum · sqlx · PostgreSQL · Redis · React · TypeScript · Docker

### 🔗 [Transit Route Optimization](https://github.com/MVMC4/transit-route-optimization)

A full-stack transit platform: a route-optimization API, an admin console,
a rider-facing app, a public marketing site and a docs site, running as
independent services behind Docker Compose with a shared PostgreSQL
database.

- **Backend:** a Node.js/TypeScript API with route CRUD and an optimization
  endpoint, backed by PostgreSQL
- **Frontend:** three separate apps (admin, rider, marketing) plus a docs
  site, each deployable independently
- **Ops:** full Docker Compose stack, SSH-deployable
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
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Ops**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

---

## Other Projects

| Project | What it is |
| --- | --- |
| [obsidian-excalidraw-low-latency](https://github.com/MVMC4/obsidian-excalidraw-low-latency) | Low-latency pen companion plugin for Obsidian Excalidraw |
| [obsidian-excalidraw-low-latency-paper](https://github.com/MVMC4/obsidian-excalidraw-low-latency-paper) | Dark/light/grid/ruled paper styles for the same |
| [obsidian-blackboard](https://github.com/MVMC4/obsidian-blackboard) | Handwritten drawings in Obsidian Canvas |
| [obsidian-sync-ios](https://github.com/MVMC4/obsidian-sync-ios) | Free, open-source iOS companion for Obsidian + Syncthing |
| [GlassHID](https://github.com/MVMC4/GlassHID) | Turns an Android phone into an offline Bluetooth keyboard/trackpad/remote/gamepad |
| [team-watch](https://github.com/MVMC4/team-watch) | Data visualization tool for scraped hackathon data |

---

## Open To

- Backend Developer (Rust / Node.js / Spring Boot)
- Frontend Developer (React / Angular)
- Full-Stack Software Engineer
- Entry-Level to Intermediate Roles

📫 **[mooketsimagwazajr@gmail.com](mailto:mooketsimagwazajr@gmail.com)**
