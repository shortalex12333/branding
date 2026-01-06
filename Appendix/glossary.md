# `/Appendix/glossary.md`

## CelesteOS — Glossary

### Purpose of this document

This glossary defines the **shared language** used across CelesteOS.

It exists to:

* prevent semantic drift
* align engineering, product, sales, and design
* eliminate SaaS ambiguity
* ensure the same words always mean the same thing

If a term is used inconsistently, trust erodes internally first — then externally.

---

## Core Terms

### CelesteOS

The full system: cloud intelligence, search interface, microactions, audit, and predictive layers.

Not:

* an app
* a chatbot
* a PMS replacement

---

### Search

The primary interface to CelesteOS.

Search is not:

* a text field
* a feature
* a filter

Search is the **entry point to orientation, decision, and action**.

---

### Situation

A resolved understanding of:

* what the user is referring to
* what exists
* what is relevant now

A situation is established **before** any action is proposed.

---

### Result Card

The atomic UI unit in CelesteOS.

A result card:

* presents state
* provides orientation
* exposes microactions

There are no “pages” in CelesteOS — only cards.

---

### Microaction

A small, explicit option a user may choose **after** orientation.

Microactions:

* never auto-execute
* never hide effects
* always preserve consent

They answer:
**“What can I do now?”**

---

### READ Action

A microaction that:

* does not change system state
* carries no risk
* executes immediately

Examples:

* View
* Open
* Show history

---

### MUTATE Action

A microaction that:

* changes reality
* requires preview
* requires signing
* produces an audit record

Examples:

* Edit inventory
* Close work order
* Submit record

---

### Mutation Ritual

The mandatory sequence for all MUTATE actions:

1. Stage
2. Preview
3. Sign
4. Commit
5. Record

No step may be skipped.

---

### Preview

A diff showing **exactly what will change** if a mutation is committed.

Preview contains:

* before → after
* no prose
* no explanation

If something cannot be previewed, it cannot be changed.

---

### Sign

The explicit act of consent.

Signing:

* binds the user to the action
* transfers responsibility
* is time-bound and scope-locked

Signing is not confirmation.
It is accountability.

---

### Record

An immutable, append-only log entry proving a mutation occurred.

Records:

* cannot be edited
* cannot be deleted
* cannot be hidden

Records exist to survive audits and incidents.

---

### Uncertainty

A state where multiple interpretations are plausible.

In CelesteOS:

* uncertainty is shown
* options are ordered
* no default is assumed

Uncertainty is never collapsed silently.

---

### Orientation

The process by which Celeste establishes:

* what it understood
* what exists
* what matters

Orientation always precedes action.

---

### Dashboard

A secondary interface used only for:

* oversight
* configuration
* review
* trend analysis

Dashboards are never the primary interface.

---

### Authority

In CelesteOS, authority means:

* restraint
* predictability
* evidence
* accountability

Authority is not confidence language or branding.

---

### Trust

Trust is the result of:

* explicit consent
* visible state
* immutable records
* correct behavior under pressure

Trust is never requested.
It is earned through structure.

---

### SaaS (Internal Term)

Used internally to describe patterns that must be avoided, including:

* feature sprawl
* dashboards-first design
* automation without consent
* persuasion-heavy copy
* novelty-driven UX

“SaaS” is a **warning label**, not a category.

---

### Canon

The complete, authoritative set of documents governing CelesteOS behavior.

If something is not in the canon, it is not guaranteed.

---

## Language Rules

+
+### Anticipation
+CelesteOS noticing the current situation and proposing the next sensible option **without executing it**.
+
+### Draft
+A staged artifact (handover draft, email draft, staged update) that is not yet a committed record.
+
+### System of Record
+The system whose signed records are considered authoritative during audits, reviews, and incidents.
+
+### Data Exhaust
+The structured traces created as a by-product of real work (searches, staged drafts, signed commits, recurring faults).
* If a new term is introduced, it must be added here
* Terms may not be redefined casually
* Marketing language must map to glossary terms internally
* Ambiguous words should be removed, not explained

---

## End of Document

---

### Self-review

* ✅ Creates shared language across teams
* ✅ Prevents semantic drift
* ✅ Reinforces non-SaaS worldview
* ✅ Useful for onboarding and reviews
* ✅ Completes the Canon cleanly

---