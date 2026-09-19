# Mooketsi Vincent Magwaza

### Full-stack engineer building useful products and the systems that keep them running

I turn early ideas into working software: the interface, API, data model,
authentication, documentation, deployment path, and operational tooling. I care
about products that solve real problems, especially where local knowledge or
everyday workflows have not yet been made easy to use.

Based in **Gaborone, Botswana**. Open to backend, full-stack, and platform-focused
opportunities.

[Email me](mailto:mooketsimagwazajr@gmail.com) ·
[View my repositories](https://github.com/MVMC4?tab=repositories)

---

## What I build

- **Product systems** — web and mobile experiences designed around a real user
  journey, not a collection of disconnected screens.
- **Backend and data platforms** — domain-focused APIs, spatial data, queues,
  caching, authentication, and databases with explicit ownership.
- **Production foundations** — observability, rate limits, security boundaries,
  recovery documentation, and deployment workflows that make a system operable.

## Selected work

### [Tsela — Gaborone transit, made searchable](https://github.com/MVMC4/transit-route-optimization)

<a href="https://github.com/MVMC4/transit-route-optimization">
  <img src="https://raw.githubusercontent.com/MVMC4/transit-route-optimization/main/docs/assets/screenshots/marketing-home.jpg" alt="Tsela marketing homepage showing its route-first transit experience" width="100%">
</a>

Tsela turns Gaborone's informal combi knowledge into a route-planning platform.
A rider can choose an origin and destination, compare road-following routes, see
where to board, and understand where to get off. The same repository includes
the rider experience, marketing site, operations dashboard, authenticated
developer portal, and API.

- FastAPI owns the HTTP API; PostgreSQL, PostGIS, and pgRouting own spatial data
  and road-aligned routing; OR-Tools supports optimization work.
- Five separate product surfaces share one platform without collapsing into one
  monolithic application.
- Prometheus, Grafana, Tempo, OpenTelemetry, structured logs, and request IDs
  provide an observable path through the system.
- The repository documents security boundaries, backups and recovery, production
  authentication, data ownership, API limits, accessibility, and launch gaps.

**Core stack:** Python · FastAPI · PostgreSQL · PostGIS · pgRouting · Next.js ·
TypeScript · Docker · Prometheus · Grafana

### [StockLink — shared purchasing for warehouses and retailers](https://github.com/MVMC4/stocklink)

| Warehouse operations | Multi-warehouse marketplace |
| --- | --- |
| <img src="https://raw.githubusercontent.com/MVMC4/stocklink/master/docs/assets/screenshots/05-warehouse-dashboard.png" alt="StockLink warehouse dashboard" width="100%"> | <img src="https://raw.githubusercontent.com/MVMC4/stocklink/master/docs/assets/screenshots/10-marketplace.png" alt="StockLink multi-warehouse marketplace" width="100%"> |

StockLink connects warehouses with retail stores, consolidates compatible demand
into bulk orders, and follows shipments through delivery. Pricing and totals are
computed on the server so the marketplace does not trust client-supplied values.

- Four Rust/Axum services—identity, commerce, notifications, and media—each own
  their PostgreSQL database behind one nginx gateway.
- Stateless JWT verification, a Redis-backed denylist and rate limiter, and
  internal-only service APIs define clear trust boundaries.
- The React application exercises the services end to end; repository Markdown
  generates the Fumadocs documentation site.
- Health-gated rolling updates run on Docker Compose. The event outbox and Kafka
  publisher are documented honestly as unfinished rather than presented as live.

**Core stack:** Rust · Axum · sqlx · PostgreSQL · Redis · React · TypeScript ·
Docker · nginx

### [GlassHID — an Android phone as an offline input device](https://github.com/MVMC4/GlassHID)

<a href="https://github.com/MVMC4/GlassHID">
  <img src="https://raw.githubusercontent.com/MVMC4/GlassHID/main/docs/images/project-banner.png" alt="GlassHID turns an Android phone into an offline keyboard, trackpad, and gamepad" width="100%">
</a>

GlassHID turns an Android phone into a Bluetooth keyboard, trackpad, media
remote, and gamepad without an account or cloud service. It uses Android's native
HID Device profile, includes a cable-only fallback, and is built with platform
APIs rather than third-party runtime dependencies.

**Core stack:** Java · Android Bluetooth HID · USB/ADB · Python

## Smaller tools and public experiments

| Project | Why it exists |
| --- | --- |
| [University CS Docs](https://github.com/MVMC4/university-cs-docs) | An open, interactive study hub for University of Botswana computer-science courses. |
| [Obsidian Excalidraw Low Latency](https://github.com/MVMC4/obsidian-excalidraw-low-latency) | A low-latency pen companion for handwritten work in Obsidian Excalidraw. |
| [Obsidian Sync for iOS](https://github.com/MVMC4/obsidian-sync-ios) | A free, open-source companion for syncing Obsidian vaults with Syncthing. |
| [Team Watch](https://github.com/MVMC4/team-watch) | A visual exploration of data collected from BOCRA hackathon teams. |

## Technical toolkit

| Area | Tools I use |
| --- | --- |
| Backend | Rust, Axum, Python, FastAPI, Java, REST APIs |
| Web | TypeScript, React, Next.js, Vite, accessible responsive UI |
| Data | PostgreSQL, PostGIS, pgRouting, Redis, SQLAlchemy, sqlx, Alembic |
| Operations | Docker, nginx, GitHub Actions, Prometheus, Grafana, Tempo, OpenTelemetry |
| Native | Android platform APIs, Bluetooth HID, Swift experiments |

## How I work

1. Start with the user journey and the facts the system must preserve.
2. Give data and service boundaries explicit owners.
3. Treat authentication, validation, rate limits, and failure states as product
   work—not a cleanup phase.
4. Document what is working, what is scaffolded, and what evidence is still
   needed before launch.
5. Prefer a small, understandable system until measured load justifies more
   infrastructure.

## What I am improving now

- Validating Tsela's route data against real Gaborone roads and rider knowledge.
- Moving authentication and operational controls from local demonstrations to a
  launch-ready deployment path.
- Finishing event delivery and deployment evidence in StockLink.
- Turning project documentation into concise engineering case studies.

## Let's talk

I am interested in teams that care about product thinking, dependable backend
systems, and engineers who can work across boundaries. I am especially happy to
walk through the decisions, trade-offs, and unfinished edges in any project
above.

**[mooketsimagwazajr@gmail.com](mailto:mooketsimagwazajr@gmail.com)**
