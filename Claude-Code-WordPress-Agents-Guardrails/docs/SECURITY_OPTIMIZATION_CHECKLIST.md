# WordPress Security & Optimization Checklist

Use this as an audit guide or client-facing checklist. Follow `policies/OPERATIONS_GUARDRAILS.md`.

## Security
- [ ] Core is up to date (or plan created)
- [ ] Plugins/themes updated; abandoned plugins removed/replaced
- [ ] Only required admin users exist; strong passwords; 2FA recommended
- [ ] Capability checks + nonces present in custom admin actions
- [ ] Input sanitized, output escaped (WPCS)
- [ ] `DISALLOW_FILE_EDIT` enabled (if appropriate)
- [ ] `WP_DEBUG` off in production; logs handled safely
- [ ] File permissions reviewed; no world-writable PHP files
- [ ] XML-RPC decision documented (disable unless needed)
- [ ] Backups + restore procedure verified
- [ ] Security plugin/WAF/CDN posture documented

## Performance
- [ ] Page cache in place (server/plugin/CDN)
- [ ] Object cache strategy decided (Redis/Memcached) if needed
- [ ] PHP OPcache enabled; PHP version supported
- [ ] Image optimization (WebP/AVIF where possible), lazyload
- [ ] CSS/JS delivery reasonable (avoid over-aggressive minification without testing)
- [ ] Autoloaded options not bloated; transients reviewed
- [ ] Cron schedule reviewed; external calls not excessive
- [ ] Core Web Vitals: LCP/INP/CLS quick wins identified

## Operational hygiene
- [ ] Staging workflow documented
- [ ] Deployment + rollback process documented
- [ ] Monitoring/logging in place (uptime, errors, security events)
