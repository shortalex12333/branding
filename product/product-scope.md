# `/Product/product-scope.md`

## CelesteOS — Product Scope

### Purpose of this document

This document defines **what CelesteOS does**, **what it explicitly does not do**, and **where the product boundary ends**.

It exists to:

* stop feature creep
* prevent parity chasing
* keep engineering focused
* protect the core model as the system scales

If a proposed feature falls outside this scope, it is rejected or deferred — regardless of demand.

---

## 1. What CelesteOS Does (Authoritative Scope)

CelesteOS provides **engineering intelligence through search**.

Specifically, CelesteOS:

* unifies all vessel engineering knowledge behind one search bar
* orients users to relevant context (systems, components, history)
* retrieves exact source material (manuals, pages, revisions)
* correlates symptoms with historical vessel data
* surfaces uncertainty explicitly
* proposes safe, contextual microactions
* enforces consent, signing, and audit on every mutation
* records every action immutably

CelesteOS turns **information chaos into decision clarity**.

---

## 2. What CelesteOS Is Optimised For

CelesteOS is optimised for:

* fault diagnosis under pressure
* inspections and audits
* handovers and crew rotation
* warranty and compliance proof
* night operations
* incomplete or ambiguous input
* tired, experienced professionals

It is not optimised for:

* data entry
* administrative workflows
* daily checklist ticking
* performance dashboards
* managerial micromanagement
+* payroll, HR, or crew admin
+* owner accounting or finance workflows
+* generic procurement / ERP tooling
+* performance dashboards as the primary interface
+* managerial micromanagement
+
+## 1.1 Anticipation Without Automation
+
+CelesteOS may propose the next sensible step based on the current situation (for example: “Add this to handover draft?”).
+
+Rules:
+
+* proposals never execute by default
+* drafting is allowed (staged, reversible)
+* publishing/submitting requires signing + a record
@@
---

## 3. What CelesteOS Explicitly Does NOT Do

CelesteOS does **not**:

* replace PMS / CMMS systems
* manage payroll or crew HR
* act as a task scheduler
* automate engineering decisions
* auto-order parts
* run background monitoring without consent
* act autonomously
* explain itself conversationally

+## 3. What CelesteOS Explicitly Does NOT Do
+
+CelesteOS does **not**:
+
+* act autonomously
+* auto-execute actions on behalf of a user
+* hide state changes or side effects
+* replace human responsibility with “AI decisions”
+* manage payroll or crew HR
+* run background monitoring **without visibility**
+* explain itself conversationally
+
+CelesteOS **does** replace traditional PMS/CMMS *as the daily work surface* by absorbing their data and making the search bar the place work happens.
+
+Legacy systems may remain as:
+
+* initial data sources during migration
+* export targets for owners/class/insurers where required
+
+But the operating goal is one system: CelesteOS.

If a feature turns Celeste into a **control panel**, it is out of scope.

---

## 4. Relationship to Existing Systems

CelesteOS assumes that vessels already have:

* PMS / CMMS software
* inventory systems
* document storage
* vendor relationships

CelesteOS does not compete with these.

It **sits above them** as an intelligence and orientation layer.
+## 4. Relationship to Existing Systems
+
+CelesteOS is designed to **absorb** existing vessel systems and datasets:
+
+* IDEA / AMOS / VOLY exports
+* inventory tables
+* work orders and fault logs
+* manuals, drawings, PDFs, photos
+* emails and notes
+
+CelesteOS treats legacy platforms as **data sources**, not places people should work.
+
+The replacement logic is simple:
+
+* users work inside CelesteOS (search → evidence → action)
+* CelesteOS writes the record with signing + audit
+* CelesteOS can export/bridge to external formats when required
+
+If a feature reintroduces “modules” or forces users back into legacy UI, it fails scope.
If CelesteOS ever duplicates a feature from those systems, it must:

* add interpretive value
* reduce cognitive load
* or expose insight those systems cannot

Parity alone is not justification.

---

## 5. The “Search Test” (Scope Gate)

Any proposed feature must pass this test:

> **Can this be naturally initiated via search?**

If the answer is “no”:

* the feature is likely out of scope
* or belongs in a different product

CelesteOS does not add features that require menus to make sense.

---

## 6. The “Pressure Test” (Reality Gate)

Ask:

* Does this help at 2am?
* Does this reduce stress during inspections?
* Does this make handovers safer?
* Does this reduce the chance of human error?

If the answer is “no”, it is not a Celeste feature.

---

## 7. Feature Requests We Will Commonly Reject

The following requests will frequently appear and should usually be rejected:

* “Can you auto-close this?”
* “Can you bulk apply these changes?”
* “Can you add a dashboard for this?”
* “Can you notify me automatically?”
* “Can you make this more like X software?”

These requests typically trade safety for convenience.

---

## 8. How New Capabilities Are Added (When They Are)

New capabilities may be added only if they:

1. Strengthen orientation
2. Preserve explicit choice
3. Improve evidence visibility
4. Do not remove human judgment
5. Do not introduce hidden state

Examples of acceptable expansion:

* better uncertainty handling
* deeper cross-system correlation
* improved source attribution
* stronger audit tooling

---

## 9. Scope Review Checklist

Before approving a new feature, answer:

1. Does this belong above existing systems, not alongside them?
2. Does this reduce thinking, not add steps?
3. Does this preserve microactions?
4. Does this avoid automation?
5. Does this reinforce trust?

If any answer is “no”, reject.

---

## End of Document

---

### Self-review

* ✅ Strong guard against feature creep
* ✅ Aligns with search-first philosophy
* ✅ Preserves premium, focused positioning
* ✅ Clear boundary for engineering and sales
* ✅ Scales without dilution

---
