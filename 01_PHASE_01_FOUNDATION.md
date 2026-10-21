# Phase 1 — Foundation

## Goal
Establish a reliable server architecture, PostgreSQL database, migrations, environment configuration, authentication and authorization without unnecessarily replacing the existing application.

## Before editing
Inspect the frontend/framework/build, hosting/deployment, routes/APIs, authentication, database/storage, tests/scripts, environment variables and production-sensitive features. Preserve viable existing choices.

## Requirements
1. Establish or document a conventional server-side API structure.
2. Connect PostgreSQL and add the initial migration.
3. Provide reproducible local database setup and useful seed/setup documentation.
4. Validate configuration at startup and provide `.env.example` with names/placeholders only.
5. Implement secure authentication or preserve existing secure authentication.
6. Enforce authorization on the server.
7. Create user/account structures supporting multiple capabilities and account status.
8. Add health/readiness checks.
9. Add consistent input validation, error handling and safe structured logging.
10. Add reasonable API rate limiting.
11. Add tests for authentication, authorization and foundation behavior.
12. Document deployment environment variables and migration steps.

## Do not
- Introduce Firestore.
- Add wallet, payments, subscriptions or financial rewards.
- Remove unrelated features.
- Commit secrets or claim readiness without evidence.

## Acceptance
A developer can reproduce the database; protected APIs enforce server-side authorization; invalid configuration fails clearly; existing build/tests remain functional or changes are documented. Review and stop before Phase 2.