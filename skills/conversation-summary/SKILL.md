---
name: conversation-summary
description: 'Summarize an inbox thread into a concise brief: status, key points, contact intent, and open items.'
---

# conversation-summary

One-line purpose: Summarize an inbox thread into a concise brief for fast SDR triage.

## When to use
When an SDR clicks 'Summarize thread' in the Copilot Panel, or when a thread grows long.

## Inputs
- Full thread messages (both directions), channel, contact metadata.

## Steps
1. Read the entire thread in order.
2. Identify current status, the contact's stated intent/need, and any objections.
3. Extract concrete open items / commitments and the most recent ask.
4. Recommend the single next step.

## Output
Return ONLY this JSON, nothing else:
`{ "summary": "2-3 sentence brief", "key_points": ["..."], "contact_intent": "...", "open_items": ["..."], "recommended_next_step": "..." }`
No prose outside the JSON. No markdown fences.