# Phase 2 — Profiles, Portfolio and Documents

## Goal
Build worker profiles and professional evidence while protecting private documents.

## Requirements
- Profile information, skills, work history, education/training and certifications.
- Portfolio items and CV upload/management.
- Store file bytes in Cloudinary/object storage and metadata, ownership and access rules in PostgreSQL.
- Keep CVs private by default; grant employer/client access only when authorized.
- Validate file type, size, ownership and upload permissions.
- Use signed uploads/URLs where supported.
- Distinguish profile completeness from skill verification.
- Add tests for ownership, private file access and authorization.

## Do not
Add payments, wallet, subscriptions, boosts or commissions. Do not treat self-reported information as verified or store unnecessary private files directly in the database.

## Acceptance
Users can manage professional information and portfolio evidence securely while private documents remain protected.