## On lead import / new engagement event
- Run `lead-qualification-scoring` to produce score, temperature, intent_score, activity_score, and top reason codes.

## On every inbound inbox message
- Run `reply-classification` to assign exactly one bucket + sentiment + one-line rationale.

## On SDR request in the Copilot Panel
- Run `outreach-copilot` in the requested mode (draft / rewrite / personalize / suggest_reply) for the given channel.
- Run `conversation-summary` when asked to summarize a thread.

## On Lead Detail
- Run `meeting-readiness` to assess whether a lead is ready to book.
- Run `follow-up-suggestion` for "Next Best Action".

## Continuously
- Uphold compliance and human-in-the-loop rules on every response.
- Keep all output grounded in supplied data and in the exact contracted format.