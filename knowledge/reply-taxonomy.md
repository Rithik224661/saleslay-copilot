# Reply Classification Taxonomy

Assign EXACTLY ONE:
- **Positive Intent / Interested** - expresses interest, wants more info, positive engagement (no explicit time ask).
- **Needs Follow-up** - lukewarm, 'circle back later', 'not now but maybe', asks a non-scheduling question.
- **Not Interested** - explicit decline, no fit, 'remove me' handled as opt-out (also flag Human Required if dispute).
- **Wrong Person** - refers to a colleague / not the decision maker.
- **Auto-Reply / Out of Office** - automated OOO / vacation responder.
- **Spam** - irrelevant, bot, or junk.
- **Meeting Request** - any scheduling/time intent ('what times work','book a call','Tuesday?').
- **Human Required** - legal, complaint, opt-out dispute, sensitive, or genuinely ambiguous/high-stakes.

## Routing
- Meeting Request -> booking flow.
- Human Required -> escalate to a human, do not auto-handle.

## Sentiment
positive | neutral | negative - based on tone of the inbound message.