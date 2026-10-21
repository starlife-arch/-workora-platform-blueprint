# Phase 7 — M-Pesa Payments and Withdrawals

## Goal
Integrate M-Pesa or another approved provider through a provider abstraction.

## Provider abstraction
Support payment initiation, status checks, verified callbacks and payouts. Inspect official provider documentation; never invent endpoints, credentials or signature mechanisms. Keep sandbox and production credentials separate.

## Payments
1. Server authorizes the request.
2. Create an internal transaction reference and idempotency key.
3. Record the payment as pending.
4. Initiate the provider request.
5. Use verified callback/status checks to determine outcome.
6. Validate amount, currency, reference and state.
7. Update payment and ledger transactionally.

The browser must never declare payment success.

## Callbacks
Authenticate/verify according to provider docs, handle idempotently, validate amount/currency/reference, log safely and protect against replay/retries.

## Withdrawals
Check KYC/payment eligibility and available funds; reserve funds atomically; submit payout; wait for verified provider outcome. Support pending, processing, success, failure, timeout and reversed/ambiguous outcomes.

## Mandatory sandbox tests
Successful payment; canceled/dismissed STK; no prompt; wrong PIN/decline; timeout; delayed callback; duplicate callback/retry; invalid callback authentication; amount/reference mismatch; browser refresh/back; lost initiation response; withdrawal success/failure/timeout/ambiguous result; concurrent duplicate attempts.

Never fake success or switch to live mode without approval.