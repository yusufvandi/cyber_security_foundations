# Week 3 — Network Layer Trust, Observation, and Control

This week focuses on the **Network Layer (Layer 3)** and how its design assumptions create both functionality and risk.

While Layer 3 enables scalable communication across networks, it does so by **implicitly trusting packet sources, routing behavior, and control-plane messages**.

---

## Weekly Focus

- Network-layer trust assumptions
- ICMP behavior and diagnostic visibility
- Packet sniffing and traffic observation
- How infrastructure can silently suppress or modify control traffic
- Defensive strategies for limiting trust and containing failure

---

## Key Lesson

Most cyber attacks do not exploit vulnerabilities —  
**they exploit assumptions.**

This week demonstrated how:
- Visibility can disappear without warning
- Control-plane protocols can be filtered or proxied
- Normal application functionality can mask underlying manipulation

---

## Defensive Perspective

Rather than relying on trust, resilient networks:
- Segment aggressively
- Limit traffic rates and privileges
- Authenticate routing where possible
- Monitor behavior continuously
- Design for partial failure and reduced visibility

---

## Repository Contents

In Week 2, the focus was on how Layer-2 protocols fail due to implicit trust.  
Week 3 expands this lesson upward:

**Lower-layer trust failures cascade into higher-layer compromise.**

Week 4 will continue exploring how these foundational assumptions affect transport and application-layer security.
