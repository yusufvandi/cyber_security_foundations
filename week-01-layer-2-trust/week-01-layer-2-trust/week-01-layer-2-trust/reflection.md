# Reflection — Rethinking Trust at the Network Foundation

### My Earlier Understanding

Before studying Layer 2 attacks, I assumed that:
- Network attacks required complex exploits
- Internal networks were mostly safe
- Security failures happened at higher layers

Layer 2 felt invisible and uninteresting.

---

### What This Study Changed

Through ARP spoofing, I realized that:
- Attacks can rely entirely on normal protocol behavior
- Trust is often implicit and inherited
- Internal networks are not inherently trustworthy

The most dangerous weaknesses are not always technical flaws, but **unchecked assumptions**.

---

### How Attackers Think at Layer 2

At this layer, attackers:
- Exploit default trust relationships
- Operate quietly inside normal traffic
- Avoid triggering alerts or errors

They do not need sophistication.
They rely on the fact that **the system expects cooperation**.

---

### A New Defensive Perspective

If I were designing or securing networks now, I would:
- Treat internal traffic as untrusted by default
- Reduce implicit trust wherever possible
- Assume local compromise is realistic

Security must begin where trust begins.

---

### How This Shapes My Thinking Going Forward

This study reframed how I view higher layers:
- Transport protocols inherit Layer 2 trust
- Applications inherit network trust
- Encryption inherits routing trust

If trust fails early, failures cascade upward.

---

### Key Insight

> Security weaknesses often originate not where systems are complex,  
> but where they are **simple and trusted**.

Understanding Layer 2 trust abuse is essential to understanding why higher-layer attacks succeed.
