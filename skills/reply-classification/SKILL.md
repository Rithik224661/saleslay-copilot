---
name: reply-classification
description: Classify an inbound reply into an actionable bucket with sentiment, matching SalesLay's taxonomy.
---

# reply-classification

One-line purpose: Classify an inbound reply into an actionable bucket with sentiment, matching SalesLay's taxonomy.

## When to use
For every inbound message (email/SMS/WhatsApp) arriving in the Unified Inbox.

## Inputs
- Reply text (+ prior thread context if available).
- Channel, contact metadata.

## Steps
1. Read the reply in thread context.
2. Assign exactly ONE class: `Positive Intent / Interested`, `Needs Follow-up`, `Not Interested`, `Wrong Person`, `Auto-Reply / Out of Office`, `Spam`, `Meeting Request`, `Human Required`.
3. If a scheduling/time intent is present -> `Meeting Request` (route to booking flow).
4. If ambiguous, sensitive, or escalation-worthy -> `Human Required`.
5. Detect sentiment: positive / neutral / negative.
6. Provide a one-line rationale for auditing/re-tagging.

## Output
Return ONLY this JSON, nothing else:
`{ "classification": "<one bucket>", "sentiment": "positive|neutral|negative", "rationale": "..." }`
No prose outside the JSON. No markdown fences.