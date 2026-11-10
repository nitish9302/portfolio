# Nitish Chauhan — Backend Systems Engineer Portfolio

> **Engineering Blueprint Drawing Sheet (NC-001)**  
> Live at: [https://nitishchauhan.dev/](https://nitishchauhan.dev/)

An engineering-first, high-precision technical portfolio designed like an ISO architectural/mechanical drafting document. Built with pure HTML5, CSS3, and native SVGs, featuring interactive system schematics, real-time concurrency flow visualizers, and dual-theme rendering (Drafting Paper & Cyanotype Blueprint).

---

## 🎯 Architecture & Design Philosophy

Rather than using generic developer templates, this portfolio is structured as a technical engineering drawing:
- **Frame & Coordinate Zones**: Border frames with coordinate margins (`A` through `F` vertically, `1` through `8` horizontally) mirroring standard aerospace and mechanical blueprint sheets.
- **Dynamic Drawing Sheet Header**: Real-time sheet indicator (`NC-001 · SHEET [N] / 4 · [SECTION TITLE]`) driven by a zero-overhead `IntersectionObserver`.
- **Dual Blueprint Engine**:
  - **Paper Mode (Light)**: Warm off-white millimetric drafting paper (`#f3f1ea`), carbon ink (`#1c1c1a`), cinnabar precision accent (`#f04800`), and 10mm/50mm coordinate grid lines.
  - **Blueprint Mode (Dark)**: Deep cyanotype blueprint navy (`#123d68`), blueprint ink (`#f1f6fc`), electric amber accent (`#ffc94d`), and blueprint grid lines.
- **Exploded Axonometric Stack (Fig. 1)**: Interactive 6-layer 3D isometric stack view with bidirectional hover synchronization between the visual layers and the Bill of Materials (Parts List) table.
- **Mechanical System Schematics**: Detailed vector circuit/pipeline diagrams for every flagship backend system with animated signal flows, decision logic, and transaction boundaries.

---

## 📐 Sheet Breakdown

```
NC-001  SHEET 1 / 4 · GENERAL ARRANGEMENT              [PAPER | BLUEPRINT]
───────────────────────────────────────────────────────────────────────────
SHEET 1: GENERAL ARRANGEMENT (GA)
  • Engineering lede, coordinates, and career positioning
  • FIG 1: Exploded Axonometric Stack View (Interactive SVG)
  • Parts List / Bill of Materials (BOM)

SHEET 2: REVISION HISTORY (EXPERIENCE & EDUCATION)
  • REV D (2024–Present): Distributed Systems & Concurrency Hardening
  • REV C (2022–2026): B.Tech Computer Science, Graphic Era Hill University (GPA 7.46)
  • REV B (2022–2023): Backend & Linux Certifications (Udemy)
  • REV A (2019–2022): CBSE Science Foundations, Kendriya Vidyalaya

SHEET 3: PRODUCTION SYSTEMS & DETAILS (DETAILS A–C)
  • DETAIL A: PgQueue — Durable Job Queue on PostgreSQL (SKIP LOCKED, Lease Reaper, DLQ)
  • DETAIL B: HookRelay — Multi-Tenant Webhook Delivery Platform (Transactional Outbox, SSRF Shield)
  • DETAIL C: SeatLock — High-Contention Seat Reservation System (Ordered Locks, SSE via LISTEN/NOTIFY)

SHEET 4: DRAWING INDEX & TITLE BLOCK
  • Drawing Index: P-01 (PgQueue), P-02 (HookRelay), P-03 (SeatLock), P-04 (Benchmark Suite), P-05 (LaTeX Résumé)
  • ISO Title Block: NC-001 specifications, 1-click email copy with tactile feedback, verified credentials
```

---

## 🛠 Featured Distributed Systems

### 1. PgQueue — Durable PostgreSQL Job Queue
* **Repository**: [`nitish9302/pgqueue`](https://github.com/nitish9302/pgqueue)
* **Stack**: Node.js, TypeScript, PostgreSQL, Docker
* **Core Mechanisms**:
  * Concurrent worker job-claiming using `FOR UPDATE SKIP LOCKED`, preventing double-processing without lock contention bottlenecks.
  * Lease-based crash recovery with worker heartbeats and an Expiry Reaper daemon recycling stalled jobs (`expires_at < NOW()`).
  * Fenced completion writes preventing resurrected workers from corrupting job state.
  * Exponential backoff with full jitter, dead-letter routing (DLQ), and transactional enqueue.

### 2. HookRelay — Multi-Tenant Webhook Delivery Platform
* **Repository**: [`nitish9302/hookrelay`](https://github.com/nitish9302/hookrelay)
* **Stack**: Node.js, TypeScript, PostgreSQL, Docker
* **Core Mechanisms**:
  * Transactional Outbox pattern guaranteeing zero lost events during process crashes by committing events, delivery records, and queue jobs in one atomic transaction.
  * SSRF ingress shield blocking private-IP ranges (RFC 1918/3927) and DNS rebinding attacks.
  * HMAC-SHA256 signature generation per subscriber endpoint.
  * Per-subscriber circuit breakers respecting `Retry-After` headers and automated replay logs.

### 3. SeatLock — High-Contention Seat Reservation System
* **Repository**: [`nitish9302/seatlock`](https://github.com/nitish9302/seatlock)
* **Stack**: Node.js, TypeScript, PostgreSQL, Docker
* **Core Mechanisms**:
  * Benchmark-backed ordered row locks eliminating deadlocks under high-contention concurrent bursts (validated with k6 across 4 concurrency models).
  * Atomic all-or-nothing multi-seat holds with automatic TTL expiration.
  * Three-phase idempotent payment confirmation and stuck-hold reconciliation daemon.
  * Real-time seat state streaming via Server-Sent Events (SSE) backed by PostgreSQL `LISTEN / NOTIFY`.

---

## 🚀 Performance & Lighthouse Standards

* **100 / 100** Performance (zero heavy third-party framework overhead, raw HTML/CSS/SVG).
* **100 / 100** Accessibility (semantic landmarks, ARIA labels, contrast-compliant colors, keyboard focus visibility).
* **100 / 100** Best Practices (secure CSP/rel headers, valid structured schema).
* **100 / 100** SEO (Schema.org `Person` JSON-LD, OpenGraph tags, canonical links).

---

## 📬 Contact & Credentials

* **Engineer**: Nitish Chauhan
* **Email**: [nitishchauhan7505@gmail.com](mailto:nitishchauhan7505@gmail.com)
* **GitHub**: [github.com/nitish9302](https://github.com/nitish9302)
* **LinkedIn**: [linkedin.com/in/nitishchauhan13](https://www.linkedin.com/in/nitishchauhan13/)
* **Portfolio**: [https://nitishchauhan.dev/](https://nitishchauhan.dev/)
* **Phone**: +91 7505102919
