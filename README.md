# Workora Platform Blueprint

Phased engineering blueprint for a Kenyan-first, mobile-first employment, skills and services platform.

Read `00_MASTER_SPEC.md` and `12_AGENT_WORKFLOW.md` before implementing any phase. Implement one phase at a time, starting with Phase 1.

Architecture direction: PostgreSQL as the authoritative database, a conventional server-side API, Cloudinary/object storage for file bytes, provider abstractions, migrations, and server-authoritative/idempotent/auditable financial operations. Do not introduce Firestore as a second source of truth.
