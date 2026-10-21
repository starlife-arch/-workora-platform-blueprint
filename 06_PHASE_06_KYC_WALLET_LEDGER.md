# Phase 6 — KYC, Wallet and Ledger

> Sensitive phase: review security and financial design before implementation.

## KYC
Support requests, evidence metadata, statuses (pending, approved, rejected, resubmission), reviewer decisions and audit history. Store evidence privately. Apply data minimization and retention rules.

Keep account status, KYC status, skill verification, employer/business verification and payment eligibility separate.

## Wallet and ledger
Use immutable financial records. Capture amount, currency, direction, type, internal reference, provider reference where applicable, status and timestamps. Use NUMERIC/DECIMAL or integer minor units, never floating point. If using double-entry accounting, enforce balanced entries.

Support available, pending, reserved and settled funds; transactions; idempotency; concurrency control; reversals/adjustments instead of destructive edits; and reconciliation-ready references. The browser must never set balances.

## Security
Restrict KYC/finance permissions. Never log raw identity documents, secrets or sensitive payment data. Do not treat screenshots as payment proof.

## Acceptance
KYC is private and auditable; ledger operations are transactional, idempotent and tested; fake paid status is impossible. Do not enable live money movement until provider integration, reconciliation and appropriate review are complete.