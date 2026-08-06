---
name: lead-qualification-scoring
description: Score a B2B lead 0-100 with a temperature and intent breakdown from firmographic + behavioral signals.
confidence: 1
usage_count: 1
success_count: 1
failure_count: 0
negative_examples: []
---

# lead-qualification-scoring

One-line purpose: Score a B2B lead 0-100 with a temperature and intent breakdown from firmographic + behavioral signals.

## When to use
On lead import (CSV or HubSpot sync) and whenever a new engagement event (open, click, reply, call outcome) arrives for a contact.

## Inputs
- Contact record: name, title, company, industry, company size, source, custom_fields.
- Behavioral signals: email opens, clicks, replies (+ sentiment), call engagement/outcome.
- Optional: agency/client ICP definition (from client workspace config).

## Steps
1. Compute a **firmographic fit** sub-score (0-40): title seniority, industry match to ICP, company size band.
2. Compute an **activity score** (0-35): weighted opens/clicks/replies/call engagement, recency-decayed.
3. Compute an **intent score** (0-25): reply sentiment + explicit buying signals ("pricing", "demo", "when can we talk").
4. Sum -> total 0-100. Map to **temperature**: >=70 Hot, 40-69 Warm, <40 Cold.
5. Return concise reason codes (top 3 drivers) for SDR transparency.

## Output
Return ONLY this JSON, nothing else:
`{ "score": 0-100, "temperature": "Hot|Warm|Cold", "intent_score": 0-25, "activity_score": 0-35, "reasons": ["...","...","..."] }`
No prose outside the JSON. No markdown fences.