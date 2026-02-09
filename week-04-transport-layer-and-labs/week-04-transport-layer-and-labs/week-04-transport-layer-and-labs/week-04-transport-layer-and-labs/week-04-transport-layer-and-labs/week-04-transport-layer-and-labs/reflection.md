# Reflection — How My View of Transport-Layer Security Changed

Earlier, I assumed that:
- Attacks relied on malformed traffic
- Encryption implied safety
- Reliability mechanisms were purely beneficial

This view was incomplete.

## What I Understand Now
I now understand that:
- Reliability requires trust
- Trust creates state
- State creates availability risk

Attackers do not need to break protocols.
They only need to consume resources honestly but excessively.

## How This Changes My Design Thinking
If designing systems today, I would:
- Limit early trust
- Expire assumptions quickly
- Design for overload, not perfection
- Treat availability as a security property

## Key Insight
Reliability and security are inseparable.
A system that cannot survive misuse cannot be considered secure.
