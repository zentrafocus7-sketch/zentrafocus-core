**Title:** ZentraFocus Core — Mission
**Purpose:** Defines the identity, boundaries, and reason for existence of ZentraFocus Core.
**Owner:** Founder (Level 0)
**Status:** Active — Constitutional
**Last Updated:** 2026-07-24
**Related Documents:** PRINCIPLES.md, GOVERNANCE.md, BLUEPRINT.md

---

# ZentraFocus Core — Mission

## 1. What is ZentraFocus Core?

ZentraFocus Core is the governance layer of the business. It is the authoritative record of what ZentraFocus has decided, standardized, and committed to — not the code that runs the business, not the content that markets it, not the data that measures it. It is the system that governs all three.

Everything else ZentraFocus builds — products, apps, campaigns, automations, agents — operates downstream of Core. Core does not operate downstream of anything.

## 2. Why does it exist?

A business run by one founder can hold its rules in memory. A business run by contractors, employees, and AI agents over a ten-year horizon cannot — memory doesn't scale, and it doesn't survive turnover.

Core exists to replace memory with record. Its job is to remove ambiguity: at any point in the company's life, any person or agent should be able to determine what is currently true, what has been decided, and who holds the authority to change it — without asking the founder directly.

## 3. What belongs inside it?

Only material that is authoritative, low-volume relative to daily operations, and expensive to get wrong:

- The constitution — mission, decision hierarchy, governance levels, lifecycle model.
- Decisions — one discrete, dated, attributed record per decision, never edited after the fact, only superseded.
- Governance rules — who may approve what, upgrade triggers as the company adds people, access policy for AI agents.
- Shared design primitives, as code — brand tokens, not brand assets.
- A registry — pointers to where every other business asset actually lives, so Core stays the index of truth without becoming the storage of everything.

If it changes daily, it does not belong here. If it is bulky, it does not belong here. If it is one team's working material rather than the whole company's shared rule, it does not belong here.

## 4. What must never belong inside it?

- Product or application source code.
- Marketing and content assets — drafts, creative, media, campaign files.
- Live business data — revenue, KPIs, funnel metrics. These are read from their systems of record; Core never holds a second, competing copy of a number that can go stale.
- Anything speculative. Core records what has been decided, never what is being considered.
- Anything that exists to serve a single product, team, or moment. Core exists to serve all of them, indefinitely.

The moment Core starts absorbing operational material, it stops being trustworthy as a source of governance and becomes just another folder of clutter. Its value is proportional to how disciplined this boundary stays.

## 5. What principles govern every future decision?

- Revenue, then customer value, then speed, then simplicity, then scalability, then documentation — this order is never reversed.
- Preserve what has already been decided. Reopen a decision only with a stated reason, never by default.
- Every addition to Core must reduce ambiguity for the next person or agent who reads it. If it doesn't, it doesn't belong here.
- Authority is scoped, not assumed. The highest-stakes material carries the highest bar for change.
- One fact lives in exactly one place. Duplication is the first sign Core is being misused.
- Build for the company's current size, structure so it can split later. Never architect for a future that hasn't arrived.

## 6. How should humans and AI agents interact with it?

The same rules, without exception for either. No one — human or agent — edits governance-level material directly; every change is a reviewable, attributed, timestamped proposal, approved at the authority level the material requires. AI agents act under scoped, least-privilege identities: they can read all of Core to inform their work, but their write access is limited to exactly what their function requires, and never extends to the constitution or governance rules themselves.

Both humans and agents are expected to check Core before acting elsewhere, and to write back to it through the same governed path when a new fact becomes decided. There is no side channel — no memory-only decision, no verbal agreement, no silent edit — that counts as authoritative until it exists in Core.

## 7. What makes this repository the Single Source of Truth?

Not its size. Core is deliberately small — most of the business lives outside it, in products, content systems, and live data platforms.

It is the source of truth because everything else defers to it. Every product, campaign, automation, and dataset answers to Core for what is currently authorized, what is current policy, and what rule governs it. Truth here is not enforced by how much is stored — it is enforced by the fact that nothing overrides Core silently, and every change to it is traceable to a specific, attributed decision.

The day something is true in practice but not reflected in Core, Core has failed at its one job. Keeping that from happening is the whole point of this repository.
