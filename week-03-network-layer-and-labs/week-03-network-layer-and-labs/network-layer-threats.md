# Network Layer Threats (Layer 3)

## Role of the Network Layer
The Network Layer (Layer 3) is responsible for:
- Routing packets between hosts
- Inter-network communication
- IP addressing (IPv4 and IPv6)
- Encapsulation of transport-layer segments

Its primary goal is **delivery**, not verification.

---

## Core Assumptions
Layer 3 operates under several implicit assumptions:
- Devices forward packets correctly
- Source IP addresses are legitimate
- Packets are not modified in transit
- Routing information is accurate

These assumptions are **not enforced by IP itself**.

---

## Trust Implications
The network layer has no native mechanism to:
- Authenticate packet origin
- Validate routing intent
- Verify path integrity

As a result, trust is assumed rather than earned.

This enables attacks such as:
- IP spoofing
- Routing manipulation
- Traffic interception
- Network-layer denial of service

---

## Key Insight
The network layer prioritizes reachability over trust.

Because higher layers depend on IP for delivery,  
**Layer-3 trust failures cascade upward**, enabling compromise beyond the network layer itself.
