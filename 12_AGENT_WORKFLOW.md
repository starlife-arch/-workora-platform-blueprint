# Coding Agent Workflow

## Before editing
1. Inspect the repository.
2. Identify framework, deployment, routes, database, authentication, storage and tests.
3. Summarize existing architecture and constraints.
4. Identify risks and compatibility concerns.
5. Make a small plan.
6. Ask only if genuinely blocked.

## During implementation
- Implement one phase only.
- Preserve existing features, data, routes and deployment.
- Do not rewrite the project merely due to preference.
- Prefer small, readable, maintainable changes.
- Put security-sensitive and business-critical logic on the server.
- Add migrations for schema changes.
- Never commit secrets.
- Do not introduce Firestore as a second source of truth.
- Use Cloudinary/object storage for file bytes and PostgreSQL for metadata/access rules.
- Treat payment, wallet, KYC, commission and subscription state as server-authoritative.
- Never fake successful payment or verification.
- Keep financial workflows auditable and idempotent.

## After implementation
Run relevant unit/integration tests, lint, type checks, build and migration checks. Inspect the final diff.

Report implementation, files changed, migrations, environment variable names, tests actually run/results, manual test steps and known risks. Do not claim tests passed unless actually run. Stop after the requested phase.

## Git workflow
Use small, scoped, reviewable commits. Do not force-push, delete branches or rewrite history without explicit authorization.