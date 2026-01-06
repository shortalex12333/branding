# `/Review & Governance/anti-patterns.md`

## CelesteOS — Anti-Patterns

### Purpose of this document

This document catalogues **patterns that must never enter CelesteOS**, even if they appear useful, modern, or industry-standard.

Most product failure does not come from bad ideas.
It comes from **reasonable shortcuts taken repeatedly**.

These anti-patterns exist to make those shortcuts unmistakable.

If a proposal matches anything in this document, it is rejected immediately.

---

## 1. The “Helpful Assistant” Anti-Pattern

### What it looks like

* Chatty responses
* Friendly reassurance
* Suggestions phrased as advice
* “I think”, “You might want to”, “Don’t worry”

### Why it’s dangerous

* Undermines professional authority
* Encourages over-trust
* Obscures responsibility

Celeste is not a companion.
It is an instrument.

### Example (Rejected)

> “It looks like you may be experiencing a generator issue. I’d recommend checking the filter.”

### Correct

> “Generator fuel pressure below operating range.
> Manual section 4.2 applies.”

---

## 2. The Automation Shortcut Anti-Pattern

### What it looks like

* “One-click fixes”
* Auto-applied recommendations
* Background execution “to save time”

### Why it’s dangerous

* Removes consent
* Removes auditability
* Creates silent failure modes

Automation without consent is negligence in regulated environments.

### Example (Rejected)

* Auto-closing a work order after a fault clears

### Correct

* “Close work order” as an explicit, signed microaction

---

## 3. The Dashboard Creep Anti-Pattern

### What it looks like

* “Overview” screens
* KPI grids
* Status panels added “for visibility”

### Why it’s dangerous

* Shifts system from action to observation
* Encourages passive monitoring
* Breaks search-first model

Dashboards rot products slowly.

### Rule

If something can be done via search, it must not be better in a dashboard.

---

## 4. The AI Theater Anti-Pattern

### What it looks like

* “AI-powered” labels
* Confidence animations
* Explanations of reasoning
* Percentages presented as certainty

### Why it’s dangerous

* Inflates perceived capability
* Invites blind trust
* Collapses uncertainty

Celeste must feel boringly correct, not impressively smart.

---

## 5. The Explanation Crutch Anti-Pattern

### What it looks like

* Tooltips explaining actions
* “Why this matters” copy
* Educational overlays

### Why it’s dangerous

* Gets ignored under pressure
* Creates false confidence
* Masks poor design

If an action needs explanation, redesign the action.

---

## 6. The Over-Confirmation Anti-Pattern

### What it looks like

* Confirm dialogs for safe actions
* Warnings for non-mutating actions
* Excessive friction everywhere

### Why it’s dangerous

* Trains users to click through warnings
* Dilutes seriousness of real commitment

Only mutation deserves ceremony.

---

## 7. The Emotional Colour Anti-Pattern

### What it looks like

* Green for encouragement
* Blue for excitement
* Red for minor errors

### Why it’s dangerous

* Introduces emotion into decision-making
* Distracts fatigued users
* Undermines authority

Colour signals state, not feeling.

---

## 8. The “Power User” Trap

### What it looks like

* Advanced modes
* Hidden shortcuts
* Optional complexity “for experts”

### Why it’s dangerous

* Fragments behavior
* Creates inconsistent outcomes
* Encourages unsafe shortcuts

Experts deserve clarity, not tricks.

---

## 9. The Silent Success Anti-Pattern

### What it looks like

* Actions completing without visible confirmation
* Background writes
* UI state changing quietly

### Why it’s dangerous

* Breaks audit trust
* Makes incident reconstruction impossible

Every mutation must leave a visible trace.

---

## 10. The Parity Panic Anti-Pattern

### What it looks like

* “Competitor X has this”
* “Industry standard feature”
* “Users expect this”

### Why it’s dangerous

* Forces Celeste into the wrong category
* Dilutes its uniqueness
* Turns it into generic software

Celeste does not chase parity.
It defines a different standard.

---

## 11. Anti-Pattern Review Test

If a proposal:

* feels faster but less explicit
* feels smarter but less accountable
* feels nicer but less serious
* feels modern but less timeless

…it is almost certainly an anti-pattern.

---

## End of Document

---

### Self-review

* ✅ Captures the most likely failure modes
* ✅ Explicitly defends trust model
* ✅ Easy to reference in reviews
* ✅ Prevents long-term erosion
* ✅ Complements decision-checklist

---
