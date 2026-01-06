# `/UX/ux-grammar.md`

## CelesteOS — UX Grammar

### Purpose of this document

This document defines the **visual and interaction grammar** of CelesteOS.

It exists to prevent:

* creative interpretation
* component sprawl
* inconsistent UI meaning
* accidental SaaS patterns

Every UI element in CelesteOS must map to **exactly one grammatical role**.

If an element does not fit a role, it does not belong in the product.

---

## 1. The Five UX Grammar Roles (Non-Negotiable)

CelesteOS uses **five and only five** UI roles:

1. **State**
2. **Action**
3. **Transition**
4. **Commitment**
5. **Record**

These roles are semantic, not stylistic.
Style follows role — never the other way around.

---

## 2. State

### What State Represents

State shows **what exists right now**.

State is factual.
State is passive.
State does not ask anything of the user.

### Examples

* Entity lines (“System: Main Engine”)
* Document references
* Inventory quantities
* Current status indicators

### Rules

* Never interactive
* Never animated
* Never emphasized for attention
* Neutral visual weight

If a user can click it, it is not State.

---

## 3. Action

### What Action Represents

Action shows **what the user may choose to do next**.

Actions are options, not instructions.

### Examples

* View
* Open manual
* Show history
* Edit inventory
* Close work order

### Rules

* Must be clearly classified as READ or MUTATE
* Must be adjacent to the State it affects
* Must not execute automatically
* Must not be visually dominant

If an action feels urgent, it is wrong.

---

## 4. Transition

### What Transition Represents

Transition shows **that something is happening**.

Transitions exist to maintain trust, not to delight.

### Examples

* “Searching manuals…”
* “Loading history…”
* “Writing update…”

### Rules

* Present tense only
* Inline with content
* Temporary
* No progress theatrics
* No spinners unless duration is unknown

If a transition feels entertaining, remove it.

---

## 5. Commitment

### What Commitment Represents

Commitment marks the moment **responsibility transfers to the user**.

This is the most serious state in the system.

### Examples

* Signature prompt
* Confirmation before commit

### Rules

* UI must pause
* Background must dim
* No other actions visible
* Cancel must remain visible

If commitment feels optional, it has failed.

---

## 6. Record

### What Record Represents

Record is **proof that something happened**.

Records exist to support:

* accountability
* audits
* review
* trust over time

### Examples

* “Updated by Alex”
* Timestamped changes
* Signed actions

### Rules

* Append-only
* Immutable
* Never editable
* Never hidden

If a record can be modified, it is not a record.

---

## 7. Role Exclusivity Rule

A UI element may belong to **one role only**.

Violations include:

* clickable state
* animated records
* actions styled as state
* transitions acting as feedback

If an element mixes roles, it must be redesigned.

---

## 8. What UX Grammar Explicitly Forbids

* Decorative UI elements
* Ambiguous affordances
* Multi-purpose components
* Emotional styling
* Gamification
* “Helpful” overlays

Every element must justify its existence through role clarity.

---

## 9. Grammar Review Checklist

Before approving a UI element, ask:

1. Which role does this serve?
2. Is that role unambiguous?
3. Does it accidentally imply another role?
4. Would a tired engineer misread this?

If unsure, reject.

---

## End of Document

---

### Self-review

* ✅ Enforces semantic clarity
* ✅ Prevents UI creativity drift
* ✅ Directly supports microactions
* ✅ Works across platforms
* ✅ Defensible under pressure

---
