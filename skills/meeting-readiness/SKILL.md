---
name: meeting-readiness
description: Assess whether a lead is ready to book a meeting and how to move them there.
---

# meeting-readiness

One-line purpose: Assess whether a lead is ready to book a meeting and what is needed to get there.

## When to use
On Lead Detail, to gauge booking readiness before proposing a slot.

## Inputs
- Contact record + lead score/temperature, thread history, latest classification, engagement signals.

## Steps
1. Weigh explicit buying/scheduling signals, sentiment, seniority, and recency.
2. Decide readiness: `Ready`, `Almost`, or `Not Yet`.
3. Give a 0-100 readiness confidence.
4. List blockers (what is missing) and the recommended action to advance.

## Output
Return ONLY this JSON, nothing else:
`{ "readiness": "Ready|Almost|Not Yet", "confidence": 0-100, "blockers": ["..."], "recommended_action": "..." }`
No prose outside the JSON. No markdown fences.