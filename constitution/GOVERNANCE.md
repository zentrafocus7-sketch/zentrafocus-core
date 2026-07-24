**Title:** ZentraFocus Core — Governance
**Purpose:** Defines who has authority over Core and the mechanism by which Core changes without losing its integrity.
**Owner:** Founder (Level 0)
**Status:** Active — Constitutional
**Last Updated:** 2026-07-24
**Related Documents:** MISSION.md, PRINCIPLES.md, BLUEPRINT.md

---

# ZentraFocus Core — Governance

This document defines how Core evolves without losing its integrity. It is deliberately a set of mechanisms, not a set of opinions — mechanisms still work when the people, tools, and technology around them change; opinions don't. Nothing here depends on any particular software, platform, or file format. If the tools ZentraFocus uses today are gone in ten years, this document should still be correct.

The governing idea: the same mechanism must work whether one person fills every role, or a hundred people and a dozen agents each fill one.

---

## Authority Levels

Authority is held by a level, not a person. Today, the Founder holds every level simultaneously — that collapse is expected and not a violation of this model. As the company grows, levels are delegated outward one at a time, never all at once.

| Level | Role | Holds |
|---|---|---|
| 0 | Founder | Sole authority over constitutional material. Cannot be delegated. |
| 1 | Maintainer | Authority over architecture and structure, within existing Principles. |
| 2 | Domain Owner | Authority over one governed domain (per the One Fact, One Owner principle). |
| 3 | Contributor | May propose changes anywhere; may approve nothing above their scope. |
| 4 | Observer | Read access only. |

A level is a responsibility, not a reward. It is assigned to match a real function and removed when that function ends.

---

## 1. Who has authority over Core?

Ultimate authority sits with the Founder (Level 0) and is non-transferable — it can be delegated in scope, never surrendered entirely, and never assumed by anyone or anything else, including an AI agent. Every other level derives its authority from an explicit grant traceable back to the Founder, directly or through a chain of delegation.

## 2. Who can propose changes?

Anyone, at any level, human or AI agent. Proposal is deliberately open — restricting who may *suggest* a change creates bottlenecks and buries good ideas. What is restricted is who may *approve* a change, which is a separate right entirely.

## 3. How are changes reviewed?

Every proposed change goes through the same four steps regardless of size: classify the change against the taxonomy below, route it to whoever holds the authority level that type of change requires, have that authority explicitly approve, reject, or defer it, and record the outcome as a dated, attributed decision. No step is skipped because the change feels small, urgent, or obvious — urgency changes how fast a review happens, never whether it happens. At solo-founder scale, the Founder performs all four steps alone; the discipline is in still performing them, not in requiring multiple people.

## 4. What types of changes exist?

| Type | Example | Required Authority | How it takes effect |
|---|---|---|---|
| Constitutional | Editing Mission, Principles, or Governance; changing the decision hierarchy | Level 0 only | Supersession — never edited in place |
| Architectural | Restructuring domains, splitting off a new repository, changing how Core is organized | Level 0, or Level 1 with Founder ratification | Requires a stated problem and a migration path before approval |
| Policy | A domain-level rule — a pricing rule, a brand standard, an agent's access scope | Level 1, or the relevant Level 2 Domain Owner | Supersession |
| Factual update | Reassigning an owner, updating a reference, routine maintenance within existing policy | The relevant Level 2 Domain Owner | In place, logged |
| Correction | Fixing an error that changes no meaning — a typo, a broken reference | Anyone with access | In place, no review required, logged if the document is constitutional |
| Operational proposal | A content, product, or automation decision that relies on Core but doesn't change it | Anyone, within existing policy | No change to Core occurs |

## 5. What requires the highest level of approval?

Anything constitutional, and anything architectural whose effects can't be cleanly reversed. This includes changing the decision hierarchy, granting a new permanent authority level, restructuring how domains are organized, and forming a new legal entity or business line. The test is not who's asking or how confident they are — per the rigor principle, the test is how hard the change would be to undo. Hard to undo means Level 0.

## 6. When does a document become constitutional?

When other approved decisions would need to be re-reviewed if it changed. The test: if this document were altered, would material built on top of it stop being trustworthy? If yes, it's constitutional, regardless of its length or how it was originally written. Mission, Principles, and this document are constitutional permanently. A new constitutional document can only be created by Level 0 approval, and only once a rule is genuinely load-bearing across more than one domain — not because a single team wants extra authority for its own rule.

## 7. When should a document be superseded instead of edited?

Whenever the change alters what was previously true. Per the irreversibility-of-record principle, that always produces a new record referencing the one it replaces — the old version is never rewritten or deleted. In-place editing is reserved strictly for corrections that change no meaning at all. The test is simple: does this change what the reader would have believed, or only how it's expressed? The former is a supersession; the latter is a correction.

## 8. When should something be archived?

When a record is superseded and no longer authoritative, or when whatever it governed — a product, a domain, a time-bound decision — no longer exists. Archiving removes something from active status without deleting it; the historical record stays intact and reachable, in keeping with the principle that Core's record outlives whatever it originally described.

## 9. When should a new repository be created?

Only when one of these specific conditions is actually met, never in anticipation of one:

- A product or domain needs a release cycle independent of everything else.
- A person or team needs access to exactly one domain, and no finer-grained access control exists to grant that without also granting the rest.
- A domain's volume or pace of change is degrading the usability of the core record for everyone else.
- A new legal entity, brand, or business line is formed that requires governance of its own.

Splitting a repository is itself an architectural change and follows that approval path — it is never done unilaterally, and never done speculatively for a future that hasn't arrived.

## 10. What conditions must be met before changing the architecture itself?

Four, in order, all required: a specific problem with the current architecture must be named — not a vague sense that something could be better; the proposed change must be checked against the Principles, particularly Single Point of Truth, Least Privilege, and Structure for Fission; a migration path for every piece of existing governed material must be defined before approval, so nothing is left orphaned; and Level 0 must approve, either directly or by explicit ratification of a Level 1 proposal. Architecture does not change because it's due for a refresh. It changes because something specific is broken.

## 11. How are AI agents governed?

Identically to humans in standard, differently only in scope, per the Principles. Concretely: every agent acts under an identity scoped to one function, never a general-purpose identity with broad standing access. An agent may propose a change at any tier, the same as a human, but may only approve or execute changes within whatever authority has been explicitly delegated to its function — an agent never elevates its own authority, and nothing ever grants an agent Level 0. Every action an agent takes against governed material is attributed to that agent's identity and reviewed under the same standard a human's action would be — not a lighter one because the agent moved faster or didn't ask for anything. An agent's scope is revisited whenever its function changes, exactly as a contractor's would be.

## 12. What actions are permanently forbidden?

- Editing or deleting a historical record. It may only be superseded.
- Self-approval of a constitutional or architectural change by the same actor who proposed it.
- Granting any AI agent constitutional (Level 0) authority, under any circumstance.
- Storing live business data inside Core as an unlabeled, undated static fact.
- Making a constitutional or architectural change without a specific, stated reason.
- Skipping the review mechanism because a change seemed obvious, small, or urgent.
- Creating a second authoritative copy of any governed fact anywhere in the system.

---

Governance here is not a committee and not a slowdown — it's four repeatable steps and five levels that already work today with one person holding all of them, and will keep working, unchanged, as that one person becomes many and some of them aren't people at all.
