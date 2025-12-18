# WP-CLI Allowlist

## Allowed without approval (read-only)
- `wp core version`
- `wp plugin status`
- `wp theme status`
- `wp user list`
- `wp option get`
- `wp config get`
- `wp site health`
- `wp transient list`
- `wp cron event list`
- `wp db size` (if available in your WP-CLI environment)

## Approval required (changes data / behavior)
- `wp plugin install|update|delete|activate|deactivate`
- `wp theme install|update|delete|activate`
- `wp core update`
- `wp search-replace`
- `wp db *`
- `wp user create|delete|promote`
- any command with `--all-tables` or `--network` (multisite-impact)
