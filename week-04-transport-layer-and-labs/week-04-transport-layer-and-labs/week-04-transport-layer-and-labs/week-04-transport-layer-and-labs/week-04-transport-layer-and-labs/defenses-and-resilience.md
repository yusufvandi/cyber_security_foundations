# Defenses and Resilience at the Transport Layer

Transport-layer defense begins with a realistic assumption:
**state can be abused before intent is verified.**

Defensive design focuses on limiting damage, not preventing all misuse.

## Controlling State Growth
Since state consumes memory and time, defenses must:
- Limit concurrent connections
- Avoid unbounded resource allocation
- Prioritize availability over completeness

## Rate Limiting and Connection Control
Rate limiting assumes:
- Trust is exploitable
- Unlimited access enables asymmetric abuse

By restricting connection attempts, systems:
- Reduce resource exhaustion
- Preserve availability during stress
- Prevent single sources from overwhelming state tables

## Timeouts and Trust Expiration
Timeouts enforce an important rule:
**prove value quickly or lose access.**

They prevent:
- Hanging connections
- Long-lived incomplete sessions
- Resource starvation

## Defense-in-Depth
No single control is sufficient.
Multiple weaker controls working together provide:
- Graceful degradation
- Predictable failure modes
- Faster recovery

## Key Insight
Transport-layer defense is about managing memory and time.
Resilient systems survive overload — they do not attempt to eliminate it.
