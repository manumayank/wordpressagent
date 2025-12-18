# WordPress Operations Guardrails (MANDATORY)

These rules override all other agent behavior in this repo.

## Default mode
- **Audit-only / read-only** unless the user explicitly approves changes.
- If environment is unknown, assume **production** and remain read-only.

## Environment rules
- Prefer **local** or **staging** for changes.
- **Production** changes require explicit user approval for each change-set.

## Backup rule
Before any of the following, you must confirm a backup/snapshot exists (or ask the user to confirm):
- WordPress core/plugin/theme updates
- database operations (including search-replace)
- edits to `wp-config.php`, `.htaccess`, web server config, or CDN/WAF rules

## Destructive / high-risk operations
The following require explicit user approval (even on staging):
- `wp plugin install|update|delete`
- `wp theme install|update|delete`
- `wp core update`
- `wp search-replace`
- `wp db optimize|repair|reset|import|export`
- user/role changes (create/delete/promote)
- disabling security plugins or changing auth-related settings

## Secrets hygiene
- Never output secrets (DB passwords, salts, API keys, tokens).
- Never commit credentials to git.
- If secrets appear in files/logs, **redact** them in outputs.

## Reporting requirements
Any approved change must include:
- what changed (exact files/commands)
- why it changed
- how to validate success
- rollback steps

## When unsure
Stop and ask for the minimum info needed (environment, access method, backup availability).
