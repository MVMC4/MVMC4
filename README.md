# Mooketsi Vincent Magwaza

### Full-stack engineer building useful products and the systems that keep them running

I turn early ideas into working software: the interface, API, data model,
authentication, documentation, deployment path, and operational tooling. I care
about products that solve real problems, especially where local knowledge or
everyday workflows have not yet been made easy to use.

Based in **Gaborone, Botswana**. Open to backend, full-stack, and platform-focused
opportunities.

[Email me](mailto:mooketsimagwazajr@gmail.com) ·
[View my repositories](https://github.com/MooketsiMagwaza?tab=repositories)

---

## What I build

- **Product systems** — web and mobile experiences designed around a real user
  journey, not a collection of disconnected screens.
- **Backend and data platforms** — domain-focused APIs, spatial data, queues,
  caching, authentication, and databases with explicit ownership.
- **Production foundations** — observability, rate limits, security boundaries,
  recovery documentation, and deployment workflows that make a system operable.

## Selected work

### [StockLink — wholesale stock, from warehouse to shop door](https://github.com/MooketsiMagwaza/stocklink)

<a href="https://github.com/MooketsiMagwaza/stocklink">
  <img src="https://raw.githubusercontent.com/MooketsiMagwaza/MooketsiMagwaza/main/assets/stocklink/stocklink-store-order-dark.png" alt="StockLink retail store view in dark mode, in a Mac window: an order in transit, with its delivery code, QR code and live position" width="100%">
</a>

<p align="center">
  <img src="https://raw.githubusercontent.com/MooketsiMagwaza/MooketsiMagwaza/main/assets/stocklink/stocklink-driver-phones-dark.png" alt="StockLink driver app in dark mode, on two iPhones: collecting a parcel with the warehouse's pickup code, then on the road with the handover form" width="76%">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/MooketsiMagwaza/MooketsiMagwaza/main/assets/stocklink/stocklink-public-tracking-dark.png" alt="StockLink public tracking page in dark mode, in a Mac window: a parcel's journey and rounded position, no account needed" width="46%">
</p>

<sub>Dark mode, from StockLink's sample-data preview: the accounts, orders and figures are invented, and each page says so. The last window is the public tracking page, which needs no account.</sub>

StockLink connects warehouses, retail stores, and delivery drivers. Stores order
from many warehouses in one cart, demand is pooled into bulk orders, and each
parcel is followed from the warehouse door to the shop. Pricing and totals are
computed on the server so the marketplace does not trust client-supplied values.

- Five Rust/Axum services—identity, commerce, notifications, media, and ops—each
  own their PostgreSQL database behind one nginx gateway.
- Stateless JWT verification, a Redis-backed denylist and rate limiter, and
  internal-only service APIs define clear trust boundaries.
- One React application serves four kinds of user—warehouse, retail store,
  phone-first delivery driver, and staff—in light and dark, with printable QR
  receipts and configurable charts.
- Every shipment carries two six-digit handover codes: a pickup code only the
  warehouse sees and a delivery code only the store sees, so a parcel cannot be
  collected or handed over without them. Public tracking shows only the journey and
  a position rounded to about 100 metres.
- Staff run the platform from an in-house admin console—accounts, sessions, API
  keys, a read-only database viewer that masks secret columns, support tickets, and
  an audit log—alongside Prometheus and Grafana, which link back to it.
- The app, the Fumadocs documentation site, and the marketing site share one
  Apple-style theme generated from the same design tokens.
- The repository says plainly what has not run: the screenshots come from a
  sample-data preview, the Docker stack and the newest migrations have never been
  brought up end to end, and the event outbox and Kafka publisher are unfinished.

**Core stack:** Rust · Axum · sqlx · PostgreSQL · Redis · React · TypeScript ·
Docker · nginx · Prometheus · Grafana

### [Tsela — Gaborone transit, made searchable](https://github.com/MooketsiMagwaza/transit-route-optimization)

<a href="https://github.com/MooketsiMagwaza/transit-route-optimization">
  <img src="https://raw.githubusercontent.com/MooketsiMagwaza/MooketsiMagwaza/main/assets/tsela/tsela-rider-routes.png" alt="Tsela rider app in a Mac window: every mapped route in Gaborone, with search and a route list" width="100%">
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

### [Obsidian Sync for iOS — local-first vault synchronization](https://github.com/MooketsiMagwaza/obsidian-sync-ios)

<a href="https://github.com/MooketsiMagwaza/obsidian-sync-ios">
  <img src="https://raw.githubusercontent.com/MooketsiMagwaza/obsidian-sync-ios/main/docs/images/vault-sync-active-session.jpg" alt="Obsidian Sync transferring an established vault on a physical iPad" width="100%">
</a>

A free, open-source iPhone and iPad companion that joins an existing Syncthing
cluster and synchronizes an Obsidian vault without a hosted account or proprietary
sync service.

- A narrow Go/Swift boundary embeds the real Syncthing engine inside a native
  SwiftUI application.
- Physical testing proved desktop-to-iPad and iPad-to-desktop transfers, including
  a deletion propagated back to the desktop.
- GitHub Actions cross-compiles the XCFramework, builds the iOS app, runs the
  linked simulator suite, and publishes an unsigned device IPA.
- The README clearly labels it a foreground-only development release and documents
  backups, signing, conflict, permission, and long-session risks.

**Core stack:** Go · Swift · SwiftUI · Syncthing · GitHub Actions

## Other technical work

| Project | Why it exists |
| --- | --- |
| [University CS Docs](https://university-cs-docs.vercel.app) | A deployed, open-source learning platform for University of Botswana computer-science courses, backed by CI, CodeQL, and reusable interactive MDX components. |
| [GlassHID](https://github.com/MooketsiMagwaza/GlassHID) | Turns an Android phone into a local-only Bluetooth keyboard, trackpad, media remote, and gamepad using native HID APIs. |
| [Obsidian Excalidraw Low Latency](https://github.com/MooketsiMagwaza/obsidian-excalidraw-low-latency) | A low-latency pen companion for handwritten work in Obsidian Excalidraw. |

## Technical toolkit

| Area | Tools I use |
| --- | --- |
| Backend | Rust, Axum, Python, FastAPI, Go, Java, REST APIs |
| Web | TypeScript, React, Next.js, Vite, accessible responsive UI |
| Data | PostgreSQL, PostGIS, pgRouting, Redis, SQLAlchemy, sqlx, Alembic |
| Operations | Docker, nginx, GitHub Actions, Prometheus, Grafana, Tempo, OpenTelemetry |
| Native | Swift, SwiftUI, Android platform APIs, Bluetooth HID |

## How I work

1. Start with the user journey and the facts the system must preserve.
2. Give data and service boundaries explicit owners.
3. Treat authentication, validation, rate limits, and failure states as product
   work—not a cleanup phase.
4. Document what is working, what is scaffolded, and what evidence is still
   needed before launch.
5. Prefer a small, understandable system until measured load justifies more
   infrastructure.

## Next up

- StockLink: its first full run on Docker, then finishing event delivery.
- Tsela: validating route data against real Gaborone roads and rider knowledge, and
  moving authentication and operational controls from local demonstrations to a
  launch-ready deployment path.
- Obsidian Sync for iOS: stress-testing interrupted transfers, conflicts,
  permissions, and larger vaults.

## Let's talk

I am interested in teams that care about product thinking, dependable backend
systems, and engineers who can work across boundaries. I am especially happy to
walk through the decisions, trade-offs, and unfinished edges in any project
above.

**[mooketsimagwazajr@gmail.com](mailto:mooketsimagwazajr@gmail.com)**
