/UX/microactions.md
CelesteOS — Microactions
Purpose of this document

This document defines what microactions are, why they exist, and how they behave.

Microactions are the core interaction model of CelesteOS.
If microactions are implemented incorrectly, Celeste becomes either:

a chatbot, or

a control panel

Both are failures.

1. What Microactions Are (Plain Definition)

Microactions are:

Small, explicit options presented to the user after Celeste understands a situation.

They are:

not commands

not automation

not shortcuts

not recommendations disguised as actions

Celeste never acts on its own.
Celeste only proposes.
The user always decides.

2. Why Microactions Exist

Once oriented, every human asks the same question:

“Okay — what can I do now?”

Microactions exist to answer that question clearly and safely.

They turn understanding into choice, without removing control.

3. The Foundational Split (Non-Negotiable)

Every microaction belongs to one of two groups.

There is no overlap.

4. Group A — READ / OBSERVE Actions
Definition

Actions that do not change system state.

Characteristics

Zero risk

Zero ceremony

Immediate execution

No confirmation

No signing

No audit requirement

Examples

View

Open

Show history

Print

Compare

Navigate to manual section

UX Rules

Rendered as plain text

Inline with content

Same visual weight as information

Execute immediately

If a READ action requires confirmation, it is misclassified.

5. Group B — MUTATE / COMMIT Actions
Definition

Actions that change reality.

This includes:

data changes

records

orders

signatures

deletions

state transitions

Characteristics

Always visible

Always deliberate

Always signed

Always logged

Never immediate

Examples

Edit inventory

Add note

Close work order

Submit record

Order part

Remove item

If an action changes anything, it is MUTATE. No exceptions.

6. The Mutation Ritual (Mandatory Flow)

Every MUTATE action follows this sequence:

1. Stage

The user selects an action.
Nothing is committed.

2. Preview

Celeste shows exactly what will change.
Only the delta. No prose.

3. Sign

User explicitly signs (passcode, biometrics, etc.).
This is the moment of consent.

4. Commit

Change is written.
UI updates inline.

5. Record

An immutable audit record is appended:

who

what

when

where

Skipping any step is a critical failure.
 
6.1 Anticipation Microactions (Contextual Prompts)
+
+CelesteOS may propose the next sensible step based on what the user is currently working on.
+
+Examples
+
+“Generator high level alarm again” → Add to handover draft
+
+“Find XYZ part” (out of stock) → Show last supplier + draft an email
+
+“Hours of work” → Prepare today’s entry for review
+
+Rules
+
+Celeste proposes — the user decides
+
+Drafting is staged, reversible, and clearly marked as not committed
+
+Publishing/submitting is a MUTATE action and follows the ritual (Preview → Sign → Commit → Record)
+

7. Cancel Behaviour (Safety Guarantee)

At every stage before Commit:

Cancel is visible

Cancel is immediate

Cancel leaves no trace

If the user cancels:

nothing is written

nothing is logged

nothing persists

8. Where Microactions Appear

Microactions are always adjacent to the thing they act on.

They never:

open new tabs

redirect to dashboards

break context

remove orientation

The interface changes beneath the search bar, not elsewhere.

9. Primary Action vs Dropdown
Primary Action

The safest meaningful READ action

Often “View” or “Open”

Dropdown (▼)

Contains all additional actions

Includes MUTATE actions

Exists for completeness, not discovery

Users ignoring the dropdown is acceptable and expected.

10. How Microactions Handle Uncertainty

If Celeste detects multiple plausible interpretations:

each interpretation gets its own microactions

ordered by confidence

no default selection

Celeste never guesses.

11. What Microactions Explicitly Do NOT Do

Microactions never:

explain themselves

justify their existence

execute automatically

hide side effects

batch multiple changes

escalate without consent

If explanation is needed, the action is poorly designed.

12. Review Checklist (Use in Implementation)

Before approving any microaction, ask:

Is it clearly READ or MUTATE?

Does it appear next to the thing it affects?

Is its impact obvious before execution?

Can the user cancel safely?

Is accountability preserved?

If any answer is “no”, reject.

End of Document
Self-review

✅ Matches original microaction philosophy

✅ Enforces safety and trust

✅ Prevents automation creep

✅ Works across mobile and desktop

✅ Reinforces calm authority