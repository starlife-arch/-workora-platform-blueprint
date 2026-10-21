# Phase 5 — Messaging, Ratings and Notifications

## Goal
Enable safe communication, reviews and reliable notifications.

## Messaging
- Conversations tied to jobs, applications, services or support cases.
- Only authorized participants may read/send messages.
- Validate messages and attachments; apply rate limits.
- Support block/report controls and moderation safeguards.

## Ratings/reviews
- Allow reviews only after an eligible interaction.
- Prevent self-review and duplicate reviews.
- Support moderation and dispute handling.

## Notifications
Provide in-app notifications and provider abstractions for email/SMS. Support delivery status, retries, idempotency, preferences and consent where required. Avoid exposing sensitive information in notification previews.

## Tests
Cover conversation membership, unauthorized access, blocking, review eligibility, duplicate reviews and notification retry/idempotency.