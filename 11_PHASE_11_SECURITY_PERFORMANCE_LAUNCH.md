# Phase 11 — Security, Performance and Launch Hardening

## Goal
Complete final hardening; do not add major new features.

## Security review
Review authentication/session/recovery, account enumeration, SQL injection, XSS, CSRF, CORS, open redirects, SSRF, rate limits, error disclosure, upload authorization/type/size, storage access/signed URLs, orphan-file cleanup, secret scanning, webhook security/replay/idempotency, financial concurrency, admin/KYC/privacy controls, audit logs and dependency vulnerabilities.

## Performance and reliability
Review query plans, indexes, N+1 queries, pagination, connection pooling, timeouts, retries, background jobs, file delivery and caching. Verify monitoring, alerts, backups, restore tests and migration recovery.

## Production checklist
Confirm environment variables; separate staging/production credentials; controlled migrations; domain/HTTPS; payment callbacks; email/SMS configuration; support channels; privacy notice; terms; pricing; refund/cancellation rules; safety guidance; account deletion/export; retention; accessibility; low-bandwidth behavior; and full test/lint/type/build results.

## Go/no-go
Classify issues as blocker, high, medium or low. Do not claim launch readiness while critical blockers remain.