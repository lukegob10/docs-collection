# Treasury Python Tooling Operating Model

**Version 1.1**

---

## Governing Principle

Control requirements scale with business reliance and financial impact.
Environment maturity follows usage maturity.

---

## Tier 0 — Local Prototype

**Environment**
Local development (e.g., Python, SQLite).

**Purpose**
Exploration and rapid prototyping.

**Restrictions**

* No recurring distribution
* No official reporting
* No financial or management reliance

**Upgrade Trigger**
Recurring or shared output → Tier 1 or above.

---

## Tier 1 — TAP Dev / VM (Development)

**Environment**
Internal Git repository + automated deployment to TAP Dev VM.

**Purpose**
Structured development and shared analytics.

**Required**

* Version control (internal only)
* Named technical owner
* Documented data sources and transformation logic

**Restrictions**
Not designated for official or recurring business reporting.

**Upgrade Trigger**
Recurring distributed reporting → Tier 1+.

---

## Tier 1+ — TAP VM Reporting (Controlled)

**Environment**
TAP Dev VM designated for reporting use.

**Purpose**
Recurring business reporting with moderate operational impact.

**Required Controls**

* Peer review prior to release
* Version tagging with retained change history
* Documented data lineage and reproducibility
* Report output archival
* Periodic validation against source systems
* Named business sponsor

**Restriction**
Not permitted for regulatory reporting or financial sign-off.

**Upgrade Trigger**
Regulatory, capital, liquidity, PnL sign-off, or executive-level reliance → Tier 2.

---

## Tier 2 — UAT / Production (Full SDLC Completion)

**Environment**
Promotion from TAP Dev → UAT → Production.

**Purpose**
Business-critical or regulated tooling.

**Required Controls**

* Formal UAT validation and sign-off
* Controlled promotion to Production
* Monitoring and logging
* Rollback capability
* Separation of development and production access

**Applies To**

* Regulatory reporting
* Financial sign-off
* Capital and liquidity decisioning
* Executive / Board materials

---

## Escalation Rule

Tool classification is determined by usage and business reliance — not infrastructure alone.
