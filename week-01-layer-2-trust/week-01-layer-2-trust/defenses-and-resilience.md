# Defenses and Resilience at Layer 2

Defensive thinking at Layer 2 must begin with a clear acknowledgment:
ARP and other local network protocols were not designed with security as a primary goal.

Effective defense, therefore, is not about “fixing” ARP, but about **reducing the impact of its trust assumptions**.

---

## Designing for Assumption Failure

A resilient Layer 2 defense assumes that:
- Devices may lie
- Traffic may be malicious but valid
- Attacks may originate from inside the network

Security at this layer is not about identifying attackers perfectly, but about **limiting how much damage trust abuse can cause**.

---

## Limiting Implicit Trust

Layer 2 defenses focus on constraining who is allowed to speak and how much they are trusted.

Common approaches include:
- Restricting which devices can claim critical roles (e.g., gateways)
- Reducing the scope of broadcast domains
- Minimizing unnecessary peer-to-peer trust

The goal is to ensure that **no single device is automatically trusted by default**.

---

## ARP-Specific Defensive Controls

Practical defensive measures include:

- **Static ARP entries**  
  Prevents spoofing for critical hosts, but does not scale well.

- **Dynamic ARP Inspection (DAI)**  
  Validates ARP replies against known IP–MAC bindings on managed switches.

- **Network segmentation**  
  Limits how far ARP-based attacks can propagate.

Each control addresses only part of the problem. None provide absolute protection.

---

## Detection and Visibility

Because prevention is imperfect, visibility becomes essential.

Monitoring can include:
- Detecting rapid or conflicting ARP replies
- Identifying frequent ARP table changes
- Alerting on unusual gateway behavior

Without visibility, Layer 2 attacks remain silent and persistent.

---

## Defense-in-Depth Begins Here

Layer 2 is the foundation of the network stack.
If trust is abused here, higher-layer protections are weakened.

Strong defense assumes that:
- Lower layers can and will fail
- Higher layers must not blindly inherit trust

---

## Key Insight

> Layer 2 defense is not about eliminating attacks.  
> It is about **containing trust** and **limiting blast radius**.

This mindset carries directly into higher layers, where trust becomes even more expensive.
