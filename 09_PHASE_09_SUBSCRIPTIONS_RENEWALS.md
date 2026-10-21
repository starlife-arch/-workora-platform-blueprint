# Phase 9 — Subscriptions and Renewals

## Goal
Add recurring plans and entitlements safely.

## Plans and states
Record plan name/version, price, currency, billing interval, entitlements and effective dates. Support pending, active, past_due, canceled, expired and payment_failed states.

## Billing safety
Activate/renew only after verified provider confirmation. Auto-renew requires appropriate user/provider consent. Clearly explain price, interval, renewal, cancellation and refund rules. Prevent duplicate charges and entitlements through idempotency. Failed or ambiguous payments must not falsely extend access.

Record plan version, provider transaction, billing periods and audit information. Enforce entitlements server-side. Provide notification preferences and relevant renewal/failure notices.

## Tests
Cover initial payment, renewal, duplicate callbacks, failed/ambiguous payment, cancellation, paid-through dates, refund/cancellation semantics and entitlement enforcement.