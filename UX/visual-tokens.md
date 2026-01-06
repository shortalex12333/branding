# `/UX/visual-tokens.md`

## CelesteOS — Visual Tokens

### Purpose of this document

This document defines the **exact visual tokens** used to express the UX grammar.

Visual tokens are **not aesthetic choices**.
They are **signals of meaning and risk**.

If tokens are misused, the system becomes misleading even if the logic is correct.

---

## 1. Token Hierarchy (Highest to Lowest Gravity)

From most serious to least serious:

1. **Commitment**
2. **Mutation**
3. **State**
4. **Read Action**
5. **Transition**

Visual weight must always respect this order.

---

## 2. State Tokens

### Meaning

Represents facts that currently exist.

### Visual Characteristics

* Neutral color
* Normal font weight
* No underline
* No hover affordance
* No iconography

### Examples

```
System: Main Engine
Component: Fuel Filter
Quantity: 12
```

### Rules

* Must never look clickable
* Must never animate
* Must never use accent color

If state attracts attention, it is wrong.

---

## 3. Read Action Tokens (Group A)

### Meaning

Safe actions that do not change state.

### Visual Characteristics

* Plain text
* Same color as body text
* Slight underline on hover only
* Inline with content

### Examples

```
View
Open manual section
Show history
```

### Rules

* Never boxed
* Never bold
* Never icon-led
* Execute immediately

If a READ action looks like a button, it is misclassified.

---

## 4. Mutation Tokens (Group B)

### Meaning

Actions that will change reality.

### Visual Characteristics

* Slight separation from content
* Lower contrast than READ actions
* Never inline
* Never default-highlighted

### Examples

```
Edit inventory
Close work order
Add note
```

### Rules

* Always require preview
* Always require signing
* Never execute directly

Mutation tokens must feel heavier **before** they act.

---

## 5. Dropdown Token (▼)

### Meaning

Reveals additional actions without forcing discovery.

### Visual Characteristics

* Small caret (▼)
* Right-aligned to primary action
* Neutral color
* No animation flourish

### Rules

* Must exist if more than one action is available
* Must contain both READ and MUTATE actions
* Must include a divider between READ and MUTATE

The dropdown exists for completeness, not encouragement.

---

## 6. Divider Token

### Meaning

Semantic separation only.

### Visual Characteristics

* Hairline thickness
* Low contrast
* Full-width within dropdown or card

### Rules

* Never decorative
* Never repeated for rhythm
* Only used to separate READ from MUTATE actions

If a divider adds visual interest, it is wrong.

---

## 7. Transition Tokens

### Meaning

Indicates that the system is currently doing something.

### Visual Characteristics

* Inline text
* Present tense
* Subtle opacity
* Auto-dismiss

### Examples

```
Searching vessel manuals…
Writing update…
```

### Rules

* No personality
* No progress bars unless time is unknown
* No spinners for known-duration tasks

Transitions must reassure through clarity, not motion.

---

## 8. Commitment Tokens

### Meaning

Marks the moment of responsibility transfer.

### Visual Characteristics

* Background dimming
* Preview content remains visible
* Signature prompt visually dominant
* No other actions visible

### Rules

* Cancel must remain visible
* No escape through clicking outside
* No soft language

This is the most serious visual state in the system.

---

## 9. Record Tokens

### Meaning

Proof that a mutation occurred.

### Visual Characteristics

* Smaller text
* Reduced contrast
* Fixed position relative to content

### Examples

```
Updated by Alex
12 Jan 2026 · 14:32
```

### Rules

* Append-only
* Never editable
* Never dismissible
* Never animated

Records must feel permanent.

---

## 10. Forbidden Visual Tokens

The following are never allowed:

* Icons for decoration
* Color to express emotion
* Shadows for emphasis
* Cards for grouping unrelated content
* Success animations
* Tooltips explaining actions

If meaning is unclear without decoration, the design is wrong.

---

## 11. Token Review Checklist

Before approving any visual element, ask:

1. Which token is this?
2. Does its weight match its risk?
3. Could it be misread under fatigue?
4. Does it accidentally encourage action?

If unsure, simplify or remove.

---

## End of Document

---

### Self-review

* ✅ Direct mapping to UX grammar
* ✅ Prevents SaaS visual creep
* ✅ Explicit enough for frontend engineers
* ✅ Supports safety-first interaction
* ✅ Scales across mobile and desktop

---
