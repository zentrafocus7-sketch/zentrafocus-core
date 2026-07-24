**Title:** Complete DECISION_TEMPLATE.md, POLICY_TEMPLATE.md, and REGISTRY_ENTRY_TEMPLATE.md field schemas
**Type:** Architectural
**Decision:** constitution/BLUEPRINT.md Section 3 states that a decision record's one job is to "prove that something specific was decided, when, by whom, and under what authority," and that a policy document's one job is to "state the single current rule for that domain." The templates created in Task 06 did not structurally support either job — both used the generic six-field metadata header (Title, Purpose, Owner, Status, Last Updated, Related Documents) with no field for the decision's content, its type, who approved it, or what it supersedes; and no field for a policy's actual rule. REGISTRY_ENTRY_TEMPLATE.md had the same gap against Section 2's definition of `registry/` as a pointer index — no field to hold the pointer itself.

This is corrected: DECISION_TEMPLATE.md now includes Type, Decision, Proposed By, Approved By, Status, Date, and Supersedes fields, matching Governance's change taxonomy and supersession mechanism. POLICY_TEMPLATE.md now includes a Policy field. REGISTRY_ENTRY_TEMPLATE.md now includes Type and Pointer fields. DOMAIN_TEMPLATE.md was already structurally sufficient (Task 08) and was not changed in shape — only its Owner field, addressed in a separate decision.
**Proposed By:** Claude (AI agent, acting as delegated Lead Architect for the v1.0 completion pass)
**Approved By:** Mohamed (Founder, Level 0) — via explicit task delegation authorizing correction of constitutional inconsistencies, confirmed by review of this completion pass
**Status:** Approved
**Date:** 2026-07-24
**Supersedes:** None — first substantive revision of these three templates since their creation in Task 06.
**Related Documents:** templates/DECISION_TEMPLATE.md, templates/POLICY_TEMPLATE.md, templates/REGISTRY_ENTRY_TEMPLATE.md, constitution/BLUEPRINT.md
