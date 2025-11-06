## Case Study — Mobile Attendance & Workforce Flexibility Platform (Appsensi)

_A mobile-first attendance solution enabling reliable check‑ins anytime / anywhere for industrial & WFA workforces_

---

### 1) Context
- Target users: operational employees in industrial sectors + distributed remote workers
- Market reality: companies needed reliable attendance logs beyond office geofence due to hybrid / WFA demands
- Business moment: post‑pandemic → attendance compliance shifted from “office presence” to “location‑agnostic trust”

### 2) Problem Statement
Traditional attendance systems were built for physical offices — they failed when employees started working from multiple locations. Data became inconsistent, HR audit trails became messy, and operational KPI reporting became unreliable.

We needed a mobile attendance system that is trusted, fast, and works anywhere.

### 3) Success Definition
Primary KPI: user adoption (monthly active attendance logs)  
Secondary KPI: engagement uplift (returning session usage)  
Time horizon: 12 months

### 4) My Role & Scope
- Product Manager — orchestrated end‑to‑end delivery
- Led 12‑person cross‑functional squad (engineering, design, QA, product ops)
- Owned feature strategy, prioritization, discovery, roadmap

---

### 5) Constraints & Realities
- Sharp cost sensitivity from industrial clients → pricing pressure
- UX must support low‑end Android devices (Indonesia market reality)
- Zero tolerance for location spoofing / fraudulent GPS signals
- Security & data trust critical → attendance data = salary impact

---

### 6) Key Decisions / Trade-offs

| Decision | Options Considered | Why We Chose This | Risk Accepted |
|---|---|---|---|
| Mobile-first vs Web-first | “Web portal + light app” vs “mobile as primary surface” | Mobile-first → WFA reality & employee location is dynamic | Requires stronger offline handling |
| Engagement model | passive clock-in/out vs UX nudges | UX nudges → improved stickiness & 20% engagement lift | Requires continuous behavioral tuning |
| Infra cost model | high-res online GPS only vs hybrid coarse+fine geolocation | Hybrid → accuracy balanced with infra cost | Complexity in validation pipeline |

---

### 7) Final Solution Summary
- Delivered a B2B/SaaS product purpose-built for distributed workforce attendance
- Mobile UX intentionally simplified around “frictionless check-in/out” flows
- Resource allocation model optimized to maximize output under budget guardrails
- Continuous collaboration loop with design & engineering to maintain velocity

Validation:
- usage tracking (daily attendance logs)
- feedback loops with customer HR
- engagement cohort curves

---

### 8) Impact
- **3,500 users** adopted within first 12 months
- **20% user engagement increase** via UX iteration strategy
- **30% margin enhancement** via resource allocation optimization
- Successful positioning as a modern attendance solution for WFA models

---

### 9) Next Iteration / What I’d do differently now
- explore audit-grade biometric validation (liveness + anti‑spoofing)
- modular policy engine (company‑specific attendance rules)
- automated anomaly detection for suspicious check-in patterns
