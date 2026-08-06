# Dispute Resolution

## Current model

Dispute resolution is currently **platform-administered**. It is not yet DAO or community-jury arbitration.

Either party can open a dispute from an eligible, non-terminal order state. The platform records the reason and makes the order, messages, attachments, and related evidence available for authorized review. Entering `disputed` freezes ordinary user transitions and the normal auto-release path.

## Decision and settlement

An authorized administrator reviews the available record and selects release to the provider or refund to the buyer. For on-chain orders, that database decision does not itself move tokens. It makes the appropriate party eligible for a signed voucher; the party then submits `claimBatch` or `refundBatch`, and the transaction/event provides settlement proof.

## What users should preserve

- A precise scope and expected delivery date.
- Platform messages and agreed changes.
- Delivery files, timestamps, and acceptance criteria.
- Relevant transaction hashes and wallet addresses.
- A concise explanation of the requested outcome.

## Known policy gaps

The reviewed source does not establish a public decision SLA, appeal procedure, evidence-retention schedule, moderator policy, or jurisdiction-specific process. These must be documented as policy before publication. Until then, label them **TODO / Unverified**, not implied guarantees.

## Roadmap

DAO voting, AI assistance, and community juries appear in forward-looking materials. They must remain labeled as roadmap concepts until deployed, governed, secured, and publicly documented.

