# `/Engineering/frontend-contract.md`

## CelesteOS — Frontend Contract

### Purpose of this document

This document defines **what the frontend is responsible for**, **what it is explicitly not allowed to decide**, and the **invariants** it must preserve.

It exists to prevent:

* UX drift during implementation
* “helpful” frontend logic
* state ambiguity
* visual behavior that undermines trust

If the frontend violates this contract, the product becomes unsafe — even if backend logic is correct.

---

## 1. The Frontend’s Role (What You Own)

The frontend is responsible for **faithful presentation**.

Specifically, the frontend must:

* render state exactly as provided
* present options without bias
* preserve ordering and confidence
* enforce the mutation ritual
* make system activity visible
* make consent explicit

The frontend does **not** interpret intent.
It does **not** improve logic.
It does **not** “help” by guessing.

---

## 2. Absolute Invariants (Never Break These)

The following rules are **non-negotiable**.

### 2.1 No Silent Mutations

* No write occurs without explicit user action
* No optimistic UI that implies success before commit
* No background updates that change visible state

If state changes, the user must see:

* the preview
* the signature
* the commit
* the record

---

### 2.2 No Collapsing Uncertainty

* If multiple interpretations exist, render all
* Preserve backend ordering
* Do not auto-select “best” options
* Do not hide lower-confidence paths

If uncertainty is collapsed in the UI, trust is broken.

---

### 2.3 No Auto-Execution

* No auto-running actions
* No “smart defaults” that commit
* No chained actions triggered by one click

One action → one outcome → one record.

---

### 2.4 No Navigation Substitution

* Do not add menus “for convenience”
* Do not redirect to dashboards
* Do not replace search with shortcuts

Search remains the primary interface.

---

## 3. What the Frontend MAY Decide

The frontend may decide **only** the following:

* spacing within defined tokens
* typography size within system scale
* responsive layout adaptations
* animation duration (within strict limits)
* focus management for accessibility

If a decision affects meaning, risk, or consent — it is **not** a frontend decision.

---

## 4. Action Rendering Rules

### READ Actions

* Render as plain text
* Execute immediately
* No confirmation
* No loading screens beyond inline status

### MUTATE Actions

* Never inline with READ
* Must trigger mutation ritual
* Must render preview exactly as provided
* Must block commit until signing completes

The frontend must never “simplify” this flow.

---

## 5. Preview Fidelity (Critical)

The preview is **sacred**.

Rules:

* Render the diff exactly as provided
* No summarization
* No prose
* No reordering
* No hiding fields

If the preview is unclear, escalate to backend.
Do not “improve” it in the UI.

---

## 6. Status & Transition Handling

* Show status immediately when work begins
* Use present tense
* Remove status on completion
* Never celebrate success visually

If the system is working, the user must see it.
If it finishes, the UI must quietly settle.

---

## 7. Error Handling Rules

Errors must:

* state what failed
* state what did *not* change
* offer a safe exit

Frontend must never:

* retry automatically
* mask errors
* reinterpret failure

---

## 8. Records & Audit Rendering

Records:

* are append-only
* are never editable
* are never dismissible
* are visually stable

The frontend must treat records as **immutable facts**.

---

## 9. Performance vs Correctness

If forced to choose:

* choose correctness over speed
* choose clarity over smoothness
* choose explicitness over convenience

Dropped frames are acceptable.
Broken trust is not.

---

## 10. Review Checklist (Frontend PRs)

Before approving a frontend change, reviewers must answer:

1. Does this preserve explicit consent?
2. Does this expose uncertainty honestly?
3. Does this change visual meaning?
4. Does this add interpretation?
5. Would a tired engineer misread this?

If any answer is “yes” → reject.

---

## End of Document

---

### Self-review

* ✅ Prevents frontend logic creep
* ✅ Protects UX grammar and microactions
* ✅ Clear ownership boundaries
* ✅ Scales with team growth
* ✅ Defends trust model

---