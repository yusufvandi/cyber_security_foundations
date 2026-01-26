# Week 01 — Layer 2 Trust and Local Network Assumptions

This phase examines how trust is established and abused at the **Data Link Layer (Layer 2)**, focusing on why attacks can succeed inside networks that are otherwise considered “secure.”

Rather than treating attacks as anomalies, this week studies how **normal protocol behavior becomes an attack surface** when trust assumptions go unchallenged.

---

## Why Layer 2 Matters

Layer 2 protocols operate inside environments typically assumed to be trusted, such as:
- Local Area Networks (LANs)
- Internal enterprise networks
- Campus or office infrastructures

Because of this perceived trust, many Layer 2 protocols prioritize:
- Speed
- Simplicity
- Automatic cooperation between devices

Security is not a primary design goal at this layer.

---

## Core Insight

Layer 2 attacks do not usually rely on malformed packets or broken implementations.

They succeed because:
- Devices trust local broadcasts
- Identity is inferred, not verified
- Cooperation is assumed by default

Protocols behave exactly as designed — attackers simply **participate dishonestly**.

---

## Topics Explored in This Phase

This week focuses on:
- Address Resolution Protocol (ARP) trust assumptions
- How identity is inferred on local networks
- Why spoofing works without violating protocol rules
- How “secure networks” can still be hostile environments

Defensive concepts are introduced not as guarantees, but as **damage-limiting mechanisms**.

---

## Defensive Perspective

Rather than aiming for perfect prevention, this phase introduces the idea that:
- Trust must be minimized
- Assumptions must expire
- Visibility matters more than blind confidence

These ideas form the foundation for all higher-layer defenses examined later.

---

## Reflection and Progression

Week 1 establishes the baseline realization that:
> Security failures often begin with trusted assumptions, not technical flaws.

This understanding becomes critical in Week 2, where the same pattern reappears at the **Transport and Application layers**, even when encryption and authentication are present.

---

## Status

✔ Conceptual foundation established  
➡ Leads directly into higher-layer trust abuse
