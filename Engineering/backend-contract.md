# `/Engineering/backend-contract.md`

## CelesteOS — Backend Contract

### Purpose of this document

This document defines **how backend systems must behave** to preserve CelesteOS’s trust model.

The backend is not a utility layer.
It is a **custodian of truth, consent, and accountability**.

If backend behavior violates this contract, **frontend correctness is irrelevant**.

---

## 1. The Backend’s Role (What You Own)

The backend is responsible for:

* determining state
* detecting uncertainty
* proposing actions
* enforcing consent boundaries
* guaranteeing audit integrity
* preventing unsafe execution

The backend does **not** optimize for convenience.
It optimizes for **correctness under scrutiny**.

---

## 2. Absolute Invariants (Non-Negotiable)

### 2.1 No Silent Mutations

The backend must never:

* mutate data without an explicit, signed request
* infer consent
* execute background writes

Every mutation must:

* be explicitly requested
* be traceable to a user
* produce a record

If a write occurs without a record, it is a critical failure.

---

### 2.2 No Collapsing Uncertainty

When multiple interpretations are possible, the backend must:

* return all plausible interpretations
* assign confidence ordering
* avoid selecting a “best” option
* avoid hiding ambiguity

The backend must **never guess on behalf of the user**.

Uncertainty is a feature, not a defect.

---

### 2.3 No Auto-Execution

The backend must never:

* chain actions
* auto-apply recommendations
* “help” by finishing flows

One request → one effect → one record.

If automation is proposed, it must be **explicitly designed as a future feature** and reviewed against principles.

---

## 3. Action Proposal Rules

The backend may **propose** actions, but never execute them.

For every proposed action, the backend must provide:

* action type (READ or MUTATE)
* scope (what it affects)
* preview payload (for MUTATE)
* reversibility (if applicable)
* audit requirements

If an action cannot be previewed, it cannot be proposed.

---

## 4. Preview Payload Requirements (Critical)

For MUTATE actions, the backend must generate a **pure diff**.

Rules:

* before → after only
* no prose
* no summarization
* no hidden fields
* deterministic ordering

The preview must be sufficient for a user to understand impact **without explanation**.

If a preview is ambiguous, the action must be rejected upstream.

---

## 5. Signing & Consent Enforcement

The backend must enforce:

* signature validation
* signer identity
* timestamping
* scope locking (what was signed is what is committed)

Signatures must:

* expire
* be bound to a specific preview
* fail safely

A signature must never be reused.

---

## 6. Commit Semantics

On commit:

* validate signature
* re-validate state
* apply mutation atomically
* generate record
* return final state

If validation fails:

* abort commit
* return failure
* guarantee no partial writes

Partial success is forbidden.

---

## 7. Records & Audit Guarantees

Every mutation must generate a record containing:

* actor (who)
* action (what)
* target (where)
* timestamp (when)
* delta (how)
* source (why is *not* stored)

Records must be:

* append-only
* immutable
* queryable
* exportable

The backend must never allow record deletion or editing.

---

## 8. Error Handling Rules

Errors must be:

* explicit
* factual
* side-effect free

The backend must:

* clearly state what failed
* clearly state what did not change
* never retry mutations automatically

If an error occurs after preview but before commit, state must remain unchanged.

---

## 9. Performance vs Safety

If forced to choose:

* choose safety over latency
* choose correctness over throughput
* choose explicitness over cleverness

A slow correct answer is acceptable.
A fast wrong action is not.

---

## 10. Backend Review Checklist

Before approving backend changes, reviewers must answer:

1. Can this mutate state without a signature?
2. Does this hide uncertainty?
3. Does this auto-execute anything?
4. Does this weaken audit integrity?
5. Would this be defensible in an investigation?

If any answer is “yes” → reject.

---

## End of Document

---

### Self-review

* ✅ Preserves trust contract end-to-end
* ✅ Aligns with frontend and UX grammar
* ✅ Enforces accountability and auditability
* ✅ Prevents dangerous automation creep
* ✅ Suitable for regulated, high-risk environments

---
