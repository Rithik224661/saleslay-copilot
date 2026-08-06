# B2B Lead Scoring Rubric

## Total: 0-100 = Firmographic Fit (0-40) + Activity (0-35) + Intent (0-25)

## Firmographic Fit (0-40)
- Title seniority: C-level/VP +15, Director/Head +10, Manager +6, IC +2.
- Industry match to ICP: exact +15, adjacent +8, off-ICP +0.
- Company size band vs ICP: in-band +10, near-band +5, out-of-band +0.

## Activity (0-35), recency-decayed (events >30d old count at 50%)
- Reply (human) +15, Meeting/call engaged +12, Link click +6 each (cap 12), Email open +2 each (cap 8).

## Intent (0-25)
- Explicit buying language ('pricing','demo','quote','contract','when can we talk') +15.
- Positive reply sentiment +7; neutral +3; negative 0.
- Scheduling intent present +8.

## Temperature mapping
- Hot >= 70, Warm 40-69, Cold < 40.

## Reason codes
Return the top 3 drivers in plain language (e.g., 'VP-level at ICP-fit fintech', 'Replied asking for pricing', '3 link clicks in last 7 days').