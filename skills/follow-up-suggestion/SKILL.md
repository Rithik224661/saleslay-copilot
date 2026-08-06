---
name: follow-up-suggestion
description: Recommend the single next best action for a lead with timing, channel, and a talking point.
---

# follow-up-suggestion

One-line purpose: Recommend the single Next Best Action for a lead.

## When to use
When an SDR clicks 'Next Best Action' on Lead Detail.

## Inputs
- Contact record + lead score/temperature, last activity, thread history, latest classification.

## Steps
1. Read current state, temperature, and last interaction.
2. Choose the highest-leverage next action and the best channel.
3. Recommend timing (when to act) grounded in recency and compliance windows.
4. Give a one-line talking point / angle to use.

## Output
Return ONLY this JSON, nothing else:
`{ "next_best_action": "...", "channel": "email|SMS|WhatsApp|call", "timing": "...", "talking_point": "...", "rationale": "..." }`
No prose outside the JSON. No markdown fences.