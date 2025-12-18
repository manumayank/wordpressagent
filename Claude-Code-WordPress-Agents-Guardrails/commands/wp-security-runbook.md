# /wp-security-runbook

Generate a **WordPress Security & Optimization Runbook** with production-safe guardrails.

## Behavior
- Do not make changes
- Use `wp-security-optimizer` for the audit
- Output a phased plan that the user can approve step-by-step
- Identify which steps require `wp-security-ops`

## Ask first (minimal)
1) Environment (local/staging/production)
2) Access method (WP-CLI+SSH vs wp-admin only vs repo only)
3) Any known constraints (maintenance window, multisite, ecommerce)

## Output
- Phase 0: data capture (read-only)
- Phase 1: P0 fixes
- Phase 2: P1 fixes
- Phase 3: P2 improvements
Each phase includes validation + rollback notes.
