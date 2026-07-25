**Title:** ZentraFocus Core — Blueprint
**Purpose:** Defines the physical repository structure that implements Mission, Principles, and Governance.
**Owner:** Founder (Level 0)
**Status:** Active — Constitutional
**Last Updated:** 2026-07-25 (registry/repositories/ broadened from source code to source code and content, per decisions/)
**Related Documents:** MISSION.md, PRINCIPLES.md, GOVERNANCE.md

---

# ZentraFocus Core — Blueprint

This document translates Mission, Principles, and Governance into a physical structure. Nothing here introduces a new rule — every directory, flow, and boundary below exists because a specific prior commitment required it. Where that's true, it's cited by name.

---

## 1. Top-Level Repository Structure

```
zentrafocus-core/
├── constitution/
├── domains/
├── decisions/
├── archive/
├── registry/
├── design-system/
└── templates/
```

Seven directories, as of the v1.0 founding commit — the original six, plus `templates/`, added by Founder decision to hold the reusable blank scaffolding for every recurring document type this repository defines. Each one exists because a distinct category of governed material was named in Mission, a distinct mechanism was defined in Governance, or — in the case of `templates/` — a distinct recurring document shape needed one consistent place to live. No two of them hold the same kind of thing. That's the whole design.

---

## 2. Purpose of Every Top-Level Directory

**`constitution/`** holds Mission, Principles, Governance, and this Blueprint — nothing else ever enters this directory. It is Level 0 only, supersession only. Mission, Principles, and Governance are permanently constitutional by Governance's own declaration; Blueprint joined them at the v1.0 founding commit, once it was recognized that the document describing Core's structure is itself load-bearing for every other governed document — the same test Governance Section 6 uses to define what counts as constitutional. Its size never grows meaningfully; if it starts to, something has been misclassified.

**`domains/`** holds one subdirectory per governed business domain, each with exactly one named owner (Principle 13 — One Fact, One Owner). This is where active policy lives — the current rule for pricing, brand, funnel, content, marketing, and agent access. This is the Policy tier from Governance's change taxonomy, approved at Level 1 or the relevant Level 2.

**`decisions/`** is the chronological, append-only ledger of every decision ever made at any tier, in the order it was made. It is the proof behind whatever is currently active in `constitution/` or `domains/` — per Principle 3 (Irreversibility of Record) and Principle 7 (Nothing Is True Until It Is Recorded), nothing becomes real until it has an entry here. Records are named `YYYY-MM-DD-short-slug.md`, keeping the ledger sortable by filename as it grows.

**`archive/`** holds retired material — a domain whose subject no longer exists, a decision whose relevance has fully expired. It's distinct from `decisions/`: the ledger keeps growing forever as history, `archive/` is where substantive material goes once it's no longer even useful as active context, so `domains/` stays lean and trustworthy for what's actually current.

**`registry/`** is the index of everything that matters to the business but doesn't live in Core — pointers to products, repositories, systems, and services, each tagged with an owner and a status. The four subdirectories are mutually exclusive by definition, not by convenience: `registry/products/` holds ZentraFocus's own sellable products; `registry/repositories/` holds source code and content repositories ZentraFocus owns, other than Core itself — including production playbooks and standards ZentraFocus has written for its own channels and products, not just code; `registry/systems/` holds third-party platforms or tools ZentraFocus depends on but doesn't own; `registry/services/` holds automations or deployed processes ZentraFocus runs. Ownership of the material is what decides repositories vs. systems; who runs the process is what decides systems vs. services. This is what keeps Core small while still being the thing everything else defers to, per Mission's closing distinction: authority isn't a function of volume.

**`design-system/`** holds shared brand primitives as reusable values, not assets. It's the one piece of substantive product material allowed inside Core, because every downstream product depends on the same primitives, and duplicating them anywhere would violate Single Point of Truth (Principle 2).

**`templates/`** holds the blank, reusable structure for each recurring document type Core defines — a decision record, a domain policy, a new domain's own DOMAIN.md, a registry entry. It contains no policy and no examples, only the empty shape a future document will take, so that shape stays consistent without being reinvented or copied from an existing filled-in document each time.

---

## 3. Responsibility of Every Core Document

**MISSION.md** answers what Core is, why it exists, and what belongs inside it. Every other document assumes this one is already true.

**PRINCIPLES.md** answers how any future decision should be judged, independent of who's making it or what tools exist at the time.

**GOVERNANCE.md** answers who is allowed to change what, and by what mechanism — it's what makes the Principles enforceable rather than aspirational.

**This Blueprint** answers where everything the above three documents describe physically lives, and why.

A record inside `decisions/` has one job: prove that something specific was decided, when, by whom, and under what authority — nothing more.

A policy document inside a `domains/` subdirectory has one job: state the single current rule for that domain, owned by exactly one role.

---

## 4. Navigation Flow for Humans

`constitution/` first, to understand the rule that governs the situation. Then the relevant subdirectory of `domains/`, to find the current, active policy. Then `decisions/`, only if the "why" behind that policy matters right now. Then `registry/`, to find where the actual work — the product, the content, the campaign — physically lives, since it never lives in Core itself.

A human leaves Core to do the work and returns to Core only to record that a decision was made. Core is a place you check and report back to, not a place you work inside.

## 5. Navigation Flow for AI Agents

Identical path, identical standard (Principle 6 — Humans and Agents Are Governed Identically), with one procedural difference: an agent resolves its own permitted scope from `domains/` programmatically, every time, before acting — never from memory of a prior grant. It then acts through the pointer in `registry/`, on the actual system, not on Core itself. If the action would change anything governed, the agent writes a proposal into `decisions/` exactly as a human contributor would; it does not alter `constitution/` or `domains/` directly, and nothing about its speed or confidence changes that requirement.

The difference between the two flows is never in what's permitted — it's that an agent's scope-check is mechanical and constant where a human's is often habitual.

---

## 6. Information Lifecycle

**Creation** — a proposal is written into `decisions/` as a dated, attributed record. Per Principle 7, it isn't real before this step, regardless of how it originated.

**Active** — once approved at the authority level Governance's change taxonomy requires, it becomes (or updates) the live version in `constitution/` or the relevant `domains/` subdirectory.

**Superseded** — when changed again, a new record in `decisions/` supersedes the old one; the old version is never edited, only replaced in the active directory while its full history remains intact (Principle 3).

**Archived** — once the subject itself is retired, its material moves out of the active directory into `archive/`. This is the only stage where something leaves the "current" surface of Core, and it never leaves the permanent record entirely.

---

## 7. Rules for Adding a New Domain

A new subdirectory in `domains/` is added only when three conditions hold together: it has exactly one nameable owner from the start (Principle 13); it governs something no existing domain already covers, with zero overlap (Principle 2 — Single Point of Truth); and its creation is itself logged as a decision before the directory is used for anything. A domain is never added speculatively — per Principle 11, it must resolve a real, current ambiguity, not anticipate a future one.

The four domains created at the v1.0 founding commit — `brand`, `product`, `marketing`, `automation` — were seeded directly by Founder authority as the initial set, standing in for the logged-decision requirement this section otherwise imposes. Every domain added after v1.0 follows the full rule above without exception.

## 8. Rules for Splitting Repositories in the Future

The same four triggers Governance defines for any new repository apply here, concretely:

`design-system/` splits out once a product needs to consume it as a versioned dependency rather than a shared reference — an independent-release-cycle trigger.

A `domains/` subdirectory splits out once its own pace of change is degrading the usability of Core for everyone else reading it.

`registry/` outgrows its current form once the number of pointers makes a flat structure unusable — a volume trigger, not a preference for something more sophisticated.

Any of these is an Architectural-tier change: it requires a named problem, a migration path for existing material, and Level 0 approval before it happens — never in advance of the trigger actually firing.

---

## 9. Relationship Between Core and Everything Else

In every case, the relationship is the same shape: Core holds the governing policy and a pointer; the thing itself lives, runs, and is stored somewhere else entirely.

**Products** — Core defines product-level policy (pricing rules, lifecycle rules). Product code, delivery, and fulfillment live in their own systems, referenced from `registry/products/`.

**Websites** — Core may define the design-system and brand standards a site must follow. The site's code and content live outside Core, referenced by pointer only.

**Marketing systems** — Core governs marketing policy — brand voice boundaries, what requires approval. Campaign assets, calendars, and channel data live in their own platforms: third-party tools are referenced from `registry/systems/`, automations ZentraFocus runs are referenced from `registry/services/`.

**Automations** — Core governs what an automation or agent is permitted to do, via the relevant `domains/` access policy. The automation's running code, credentials, and logs live in their own service, entirely outside Core, referenced from `registry/services/`; the automation reads its permitted scope from Core before acting, every time.

**External storage** — live data, analytics, and media are never copied into Core as static fact (Principle 10). Core holds, at most, a pointer to the system of record, and if a historical snapshot is ever needed, it lives in `archive/`, explicitly dated, never presented as current.

---

## 10. What Core Explicitly Refuses to Become

Core will not become a content library, a media store, a live analytics dashboard, a project management tool, or any place where day-to-day work actually happens. It will not grow in proportion to the business — its size should stay roughly flat while everything it governs multiplies around it. A domain, a decision, a pointer, a template: that's the entire vocabulary of what belongs here.

Mission already states the first failure mode: something is true in practice but not reflected in Core. This blueprint names the second, equal failure mode: Core is holding material it should only be pointing at. Either one means Core has stopped doing its one job.

Built correctly, nothing here should feel like a decision at all ten years from now — just the obvious place a rule, a policy, or a pointer was always going to live.
