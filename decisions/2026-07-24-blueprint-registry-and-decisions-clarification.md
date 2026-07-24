**Title:** Resolve registry/ subtype ambiguity and establish decisions/ naming convention
**Type:** Constitutional
**Decision:** constitution/BLUEPRINT.md Section 2 previously described `registry/` as holding "pointers to products, systems, repositories, and services" with no stated rule for which subtype a given pointer belonged in. Section 9 compounded this with an explicit hedge: marketing platforms were "referenced from `registry/systems/` or `registry/services/` as applicable" — leaving the actual choice undefined. This is corrected: Section 2 now states a deterministic rule (ownership of the code decides repositories vs. systems; who runs the process decides systems vs. services), and Section 9's hedge is replaced with the concrete rule (third-party tools → `registry/systems/`; automations ZentraFocus runs → `registry/services/`). Section 2 also now specifies a `decisions/` file-naming convention — `YYYY-MM-DD-short-slug.md` — which did not previously exist, so the ledger stays sortable by filename as it accumulates entries over years.

Prior wording, for the record: registry/ paragraph read "pointers to products, systems, repositories, and services" with no subtype criteria; the marketing paragraph read "referenced from `registry/systems/` or `registry/services/` as applicable"; no naming convention was stated for decisions/.
**Proposed By:** Claude (AI agent, acting as delegated Lead Architect for the v1.0 completion pass)
**Approved By:** Mohamed (Founder, Level 0) — via explicit task delegation authorizing correction of constitutional inconsistencies, confirmed by review of this completion pass
**Status:** Approved
**Date:** 2026-07-24
**Supersedes:** None — no prior decision record set the original ambiguous language; it originated as an unreviewed gap in the v1.0 founding commit (Tasks 05–06), not a deliberate prior decision.
**Related Documents:** constitution/BLUEPRINT.md, templates/REGISTRY_ENTRY_TEMPLATE.md, templates/DECISION_TEMPLATE.md
