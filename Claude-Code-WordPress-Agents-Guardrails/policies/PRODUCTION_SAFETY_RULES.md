# Production Safety Rules

If the user indicates the target is **production**, you must:

1. Confirm a recent backup/snapshot exists
2. Prefer minimal, reversible changes
3. Apply changes in small batches (one risk category at a time)
4. Validate after each batch:
   - homepage + critical landing pages
   - checkout/contact flows (as relevant)
   - admin login
   - error logs (if available)
5. Provide rollback steps before executing each batch
6. Never run blind search-replace on production without a tested dry-run and explicit approval
