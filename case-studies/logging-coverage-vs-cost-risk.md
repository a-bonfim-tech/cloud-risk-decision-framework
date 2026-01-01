# Case Study — Logging Coverage vs Cost Risk

## 1) Context

A cloud environment supports multiple workloads with varying criticality.
Centralized logging is required for security visibility, audit readiness, and
incident investigation.

The organization operates under cost constraints and experiences periodic
traffic spikes that significantly increase log volume.

Constraints:

* Audit and compliance expectations exist
* Cost predictability is required
* Security team resources are limited
* Not all workloads have equal risk profiles

## 2) Risk Hypothesis

Insufficient logging coverage increases the risk of:

* Undetected security incidents
* Inability to reconstruct events post-incident
* Audit findings due to lack of evidence

Excessive logging, however, introduces:

* Cost overruns
* Signal dilution
* Operational overload without proportional risk reduction

The core risk is **misalignment between visibility and actual risk exposure**.

## 3) Options Considered

**Option A — Full logging everywhere**
Enable maximum logging across all workloads.

**Option B — Minimal logging**
Log only critical authentication and perimeter events.

**Option C — Risk-tiered logging strategy**
Adjust logging depth based on workload criticality and threat exposure.

**Option D — Delay logging optimization**
Accept current state and revisit after cost or audit pressure.

## 4) Trade-offs

* Option A maximizes visibility but introduces uncontrolled cost growth.
* Option B reduces cost but creates blind spots during investigations.
* Option D postpones effort but compounds long-term risk.
* Option C requires governance discipline but balances visibility and cost.

## 5) Decision

**Option C — Risk-tiered logging strategy** was selected.

## 6) Rationale

Logging is treated as a **risk control**, not a default configuration.

The decision acknowledges that:

* Not all assets require the same level of visibility
* Audit defensibility depends on intent and documentation, not volume
* Cost control is part of security governance

The objective is to ensure that **high-risk events are always observable**,
while low-risk noise is intentionally reduced.

## 7) Controls / Guardrails (Abstract)

* Asset classification and risk tiers
* Minimum logging baselines per tier
* Cost monitoring thresholds
* Explicit acceptance of reduced visibility where justified

Controls are reviewed periodically and adjusted as risk changes.

## 8) Evidence & Traceability

* Risk classification documentation
* Audit requirements mapping
* Cost impact assessments
* Logging rationale records

This decision is defensible even when incidents occur outside full visibility.

## 9) Review & Expiry

* Decision date: documented at approval time
* Review trigger: audit request, incident, or cost anomaly
* Expiry date: aligned with architecture or compliance changes
