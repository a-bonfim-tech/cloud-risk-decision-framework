# Case Study — Public API Exposure Risk

## 1) Context

A cloud-hosted application exposes a public-facing API used by external clients.
The system handles non-classified business data but operates under regulatory and
reputational constraints.

The platform is cloud-native, internet-facing by design, and expected to scale
with unpredictable traffic patterns.

Constraints:

* Availability is a business requirement
* Regulatory exposure exists, but no strict data residency mandate
* Operational overhead must remain low
* Security team capacity is limited

## 2) Risk Hypothesis

A publicly exposed API increases the risk of:

* Abuse through automated requests
* Credential stuffing or token misuse
* Unintended data exposure through misuse of legitimate endpoints
* Cost amplification through traffic-based billing

The primary concern is not data theft, but **loss of control over access patterns**
and the inability to distinguish legitimate usage from abuse.

## 3) Options Considered

**Option A — Full exposure with minimal controls**
Rely on basic authentication and reactive monitoring.

**Option B — Aggressive restriction**
Limit access through strict IP allowlists or private connectivity only.

**Option C — Controlled public exposure with layered safeguards**
Maintain public access while enforcing identity-aware and behavior-based controls.

**Option D — Delay exposure**
Postpone public access until additional organizational maturity is achieved.

## 4) Trade-offs

* Option A reduces complexity but increases operational and financial risk.
* Option B improves security posture but conflicts with business scalability.
* Option D reduces immediate risk but blocks product delivery.
* Option C introduces moderate complexity but balances availability, control,
  and auditability.

## 5) Decision

**Option C — Controlled public exposure with layered safeguards** was selected.

## 6) Rationale

The decision prioritizes **risk containment over risk elimination**.

Public exposure is acknowledged as a business necessity. The chosen approach
accepts this reality while focusing on:

* Identity-aware access boundaries
* Behavioral visibility instead of perimeter denial
* The ability to explain and defend the decision during audits or incidents

The goal is not to prevent all abuse, but to **retain decision control**.

## 7) Controls / Guardrails (Abstract)

* Identity-based access enforcement
* Request-level logging and correlation
* Rate limiting and anomaly thresholds
* Clear ownership for access policy decisions
* Explicit acceptance of residual risk

No control is assumed to be perfect or permanent.

## 8) Evidence & Traceability

* Architecture decision records (ADR)
* Risk acceptance notes
* Monitoring and alerting rationale documentation

This decision is traceable to governance requirements, not tooling defaults.

## 9) Review & Expiry

* Decision date: documented at approval time
* Review trigger: traffic pattern change, incident, or audit request
* Expiry date: aligned with major platform or business changes
