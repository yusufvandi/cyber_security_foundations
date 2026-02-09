# Week 4 — Transport Layer Trust, State, and Availability

In previous weeks, I examined how trust failures at lower layers (ARP at Layer 2 and IP at Layer 3) enable attackers to blend into normal system behavior rather than break protocols.

This week focuses on the **Transport Layer (Layer 4)** — where reliability, state, and time are introduced.

The transport layer enables dependable communication by:
- Maintaining connection state
- Allocating memory and buffers
- Managing retransmissions and flow control

These mechanisms improve reliability, but they also introduce **asymmetric cost and availability risk**.

Through conceptual study and packet observation, this week explores:
- How TCP establishes trust before verifying intent
- Why stateful design makes availability fragile
- How encrypted traffic can still exhaust system resources
- Why transport-layer defenses focus on time, memory, and trust expiration

This week reinforces a central insight of this project:
**Security failures rarely come from broken protocols — they come from trusted design assumptions held too long.**
