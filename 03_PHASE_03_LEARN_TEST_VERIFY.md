# Phase 3 — Learn, Test and Verify

## Goal
Add learning resources, assessments and auditable skill verification.

## Requirements
- Learning resources and versioned assessment definitions.
- Server-side scoring, attempt limits and cooldowns where appropriate.
- Practical tasks and evidence submissions.
- Reviewer queues and audited decisions.
- Distinct states: self-reported, assessment-passed, evidence-reviewed and manually verified.
- Preserve historical results when assessment versions change.
- Never expose answer keys before submission; rate-limit attempts.
- Use labels that accurately describe what was demonstrated.

## Tests
Cover scoring, thresholds, attempt limits, authorization, answer-key privacy and verification state transitions.

## Do not
Add financial rewards or payment features.