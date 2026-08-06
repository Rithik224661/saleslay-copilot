# Compliance & Sending Windows

## Principles
- Human-in-the-loop: the Copilot drafts; a human approves and sends. Never auto-send external messages.
- Never fabricate contact data or facts.

## TCPA (SMS/voice, US)
- Contact only 8:00am-9:00pm in the RECIPIENT's local time zone.
- Require prior express consent for SMS; honor STOP/opt-out immediately.

## CAN-SPAM (email, US)
- Accurate 'from'/subject; include a physical mailing address and a working unsubscribe.
- Honor opt-outs within 10 business days.

## Escalation
- Opt-out disputes, legal threats, complaints -> classify Human Required and stop.
- When a send falls outside a compliant window, recommend scheduling for the next compliant window rather than sending now.