# `/UX/canonical-screens/README.md`

## CelesteOS — Canonical Screens

### Purpose of this document

This document defines the **canonical reference screens** for CelesteOS.

These screens are not mockups for exploration.
They are **ground truth**.

If an implementation diverges from these screens, the implementation is wrong — even if it “looks better”.

---

## How to Use This Folder

* Each screen represents a **contract**, not a suggestion
* Engineers build to these behaviors
* Designers refine *within* these constraints, never outside them
* Any new screen must be explicitly justified against these canonicals

This folder intentionally contains **very few screens**.

CelesteOS is not a screen-based product.

---

## Canonical Screen List (Complete)

There are **five** canonical screens.
No others are permitted without explicit review.

---

## 1. Search Empty State

### Purpose

Establish calm, authority, and readiness — without instruction.

### Characteristics

* Single global search bar
* No illustrations
* No examples
* No onboarding copy
* No call-to-action language

### Rules

* The system does not tell the user what to ask
* The system does not explain itself
* The system waits

### Success Criteria

A tired engineer immediately understands:

> “I can type anything here.”

If the screen teaches, it has failed.

---

## 2. Single Result Card — READ Only

### Purpose

Demonstrate orientation without risk.

### Structure

* Header: What this is
* Body: Minimal useful truth
* Primary READ action
* Dropdown available if more actions exist

### Characteristics

* No confirmation
* No modal
* Immediate execution
* Inline update

### Rules

* READ action must execute instantly
* Status line appears inline
* Result replaces itself with content

### Success Criteria

User can act without thinking about consequences.

---

## 3. Single Result Card — With MUTATE Action

### Purpose

Demonstrate safe, deliberate change.

### Structure

* Same as READ card
* MUTATE action available via dropdown or secondary position

### Flow (Mandatory)

1. Action selected
2. Stage (no change)
3. Preview (diff only)
4. Sign
5. Commit
6. Record appears

### Rules

* No shortcuts
* No skipping preview
* No bundling actions

### Success Criteria

User always knows:

* what will change
* when it changes
* who is responsible

---

## 4. Uncertainty Split

### Purpose

Show how Celeste handles ambiguity without guessing.

### Structure

* Two or more interpretations
* Equal visual weight
* Ordered by confidence
* Each with its own actions

### Characteristics

* No default selection
* No recommendation language
* No “Did you mean?”

### Rules

* User must choose explicitly
* Non-selected options disappear after choice
* No confirmation language

### Success Criteria

Uncertainty feels normal, not alarming.

---

## 5. Mobile Equivalent (Vertical Flow)

### Purpose

Prove that the model is universal across form factors.

### Characteristics

* Same logic as desktop
* Vertical stacking
* No feature loss
* No “mobile simplifications”

### Rules

* Search still primary
* Microactions still explicit
* Mutation ritual unchanged

### Success Criteria

Mobile feels smaller, not different.

---

## What Is Explicitly Not Canonical

The following are **not** canonical and must not be introduced:

* dashboards as primary UI
* settings-first flows
* navigation menus
* chat-style interfaces
* tutorials embedded in UI
* multi-pane layouts

If a screen looks like SaaS, it is wrong.

---

## Adding a New Canonical Screen (Rare)

A new canonical screen may only be added if:

1. It cannot be expressed through search
2. It preserves orientation → decision → action
3. It does not introduce navigation
4. It does not bypass microactions
5. It passes the decision checklist

If unsure, do not add it.

---

## Canonical Review Checklist

Before approving an implementation against these screens:

* Does it behave the same?
* Does it feel calmer?
* Does it expose the same risks?
* Does it preserve consent?
* Does it reduce cognitive load?

If any answer is “no”, revise.

---

## End of Document

---

### Self-review

* ✅ Translates doctrine into concrete reference
* ✅ Prevents screen explosion
* ✅ Keeps search as the interface
* ✅ Enforces microaction ritual
* ✅ Scales across desktop and mobile

---
