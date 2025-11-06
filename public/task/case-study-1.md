## Case Study — Corporate Health Benefits Platform (Prixa)

_A digital-first SaaS that centralizes corporate health benefits into one seamless platform_

---

### 1) Context
- Target user: employees of enterprise clients (corporate health benefit users)
- Business environment: fragmented health journeys — employees accessing different providers across different channels → poor experience + high cost
- Timing: corporate clients started demanding measurable ROI & simplicity (post-COVID shift, heavy focus on cost efficiency)

### 2) Problem Statement
Employees and HR teams were struggling with a fragmented healthcare experience. They bounced between multiple apps, providers, and manual processes — causing low usage, low visibility, and high claim inefficiency.

We needed to unify the experience into a **single** digital entry point.

### 3) Success Definition
Primary KPI: User activation & usage (MAU / activation funnel)  
Secondary KPI: cost efficiency (infrastructure + delivery)  
Time horizon: 3 months post-launch for first measurable adoption wave

### 4) My Role & Scope
- Product Manager — responsible for strategy, problem framing, requirement definition, prioritization, stakeholder alignment
- Directed ~25 cross-functional team members (engineering, design, QA, ops, infra)
- Scope across legacy improvement + new product delivery

---

### 5) Constraints & Realities
- Must continue supporting legacy stack (zero downtime allowed)
- Limited infrastructure budget (cost pressure)
- Extremely fast delivery window — first enterprise prospect pipeline already waiting
- Strict compliance/legal requirements (health data)

---

### 6) Key Decisions / Trade-offs

| Decision | Options Considered | Why we chose this | Risk Accepted |
|---|---|---|---|
| Unified app vs separate modules | “Add modules to legacy” vs “build clean new SaaS” | New SaaS → easier to iterate, modern UX, clean data model | Migration friction + dual system period |
| Incremental rollout scope | Full feature parity vs prioritized 80/20 | Ship 80% value first → faster time to market | Some stakeholders initially unhappy re: missing minor things |
| Infra cost model | Auto-scale infra vs reserved capacity | Optimized reserved capacity → 50% cost cut | Needed careful forecasting + usage modeling |

---

### 7) Final Solution Summary
- Delivered a single corporate health benefit SaaS product
- Prioritized + shipped 45+ new features & bug fixes
- Implemented Agile rituals + prioritization discipline to remove internal bottlenecks
- Optimized infra + delivery model to drastically reduce costs

Validation:
- feature usage analytics
- cohorts on activation
- client feedback loops (direct with HR teams)

---

### 8) Impact
- **2,500 new users** within 3 months post-launch
- **50% faster time-to-market** for new features
- **50% cost reduction** in infra + dev spend
- Legacy tech debt reduced while shipping net-new product

---

### 9) Next Iteration / What I’d do differently now
- introduce pricing experimentation (per member / per claim / per company tiering)
- stronger AB testing protocols earlier
- invest in modular configurable benefit packages to accelerate enterprise onboarding
