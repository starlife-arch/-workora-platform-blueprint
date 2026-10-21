# Workora Master Specification

## Product goal
Build a trustworthy, mobile-first, low-bandwidth-friendly platform for Kenya where people discover work, demonstrate practical skills, offer services and manage work-related transactions, with future international expansion possible.

## Core capabilities
- Worker and employer/client accounts; one person may hold both capabilities.
- Profiles, skills, work history, portfolios, CVs and certificates.
- Learning resources, practical assessments and skill verification.
- Formal jobs, casual/day jobs, gigs and service listings.
- Applications, shortlisting, hiring and work-status tracking.
- Messaging, notifications, ratings/reviews and reports.
- Identity/business verification and moderation.
- Wallet, deposits, withdrawals, commissions, subscriptions, boosts and referrals.
- Admin operations and analytics.

## Architecture
- Inspect and preserve a viable existing frontend, routes and deployment.
- Use a conventional server-side API.
- PostgreSQL is the authoritative application database; use versioned migrations.
- Store file bytes in Cloudinary/object storage; store metadata, ownership and access rules in PostgreSQL.
- Do not add Firestore as a second source of truth.
- Use provider adapters for payments, email, SMS and storage.
- Use background jobs for retries, notifications, expiry and renewals.
- Keep secrets in environment variables or a secrets manager, never in Git.

## Database conventions
Use constraints and transactions for critical state changes; UUIDs or non-guessable public IDs where appropriate; UTC timestamps; indexes based on real queries; pagination; server-side validation; and explicit transaction boundaries. Represent money using NUMERIC/DECIMAL or integer minor units, never floating point. Use soft deletion only when justified.

## Security and privacy
Enforce authorization server-side. Protect sessions and account recovery. Use appropriate rate limits, CSRF/CORS protections and upload validation. Follow least privilege. Keep CVs, KYC evidence and payment information private by default. Define retention/deletion rules. Audit sensitive actions. Never log passwords, secrets, tokens or unnecessary sensitive data. Provide abuse/report/block controls where appropriate.

## Financial safety
The browser must never be authoritative for wallet balances, payment status/references/amounts, KYC eligibility, subscription entitlements, commissions or withdrawal completion. Verified provider callbacks and/or status checks determine payment outcomes. Never fake success.

Support idempotency, immutable ledger entries, reversal/adjustment records, concurrency control, replay/double-spend protection, pending versus settled funds, provider references and reconciliation. Test cancellation, timeout, wrong PIN/decline, delayed/duplicate/missing callbacks and ambiguous outcomes.

## UX
Mobile-first, accessible and low-bandwidth friendly. Show clear pending/success/failure states. Do not overclaim verification. Explain fees, subscriptions, boosts, referral terms and withdrawal rules. Separate customer and administrative interfaces by authorization.

## Quality gates for every phase
1. Inspect the repository and summarize architecture/constraints.
2. Plan a single phase only.
3. Implement that phase; add migrations and tests.
4. Run relevant tests, lint, type checks and build.
5. Inspect the diff.
6. Report changes, migrations, environment variables, tests actually run, manual steps and risks.
7. Stop before the next phase.

## Compliance
Before production, obtain appropriate legal/accounting review for employment/recruitment, consumer protection, privacy/data protection, KYC, tax, payments/stored value, referral incentives and subscriptions.