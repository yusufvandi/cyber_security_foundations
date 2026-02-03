# Defenses and Resilience at the Network Layer (Layer 3)

Effective defense at the network layer begins with a realistic assumption:

**Malicious traffic can originate from anywhere — including inside the network.**

Layer-3 defenses are not about perfect prevention.  
They focus on **containment, reduced trust, and sustained availability**.

---

## Control Through Boundaries
Resilient networks avoid location-based trust.

Principles:
- Treat internal and external traffic as potentially hostile
- Avoid assuming safety based on IP address alone

Boundaries reduce the blast radius of failure.

---

## Segmentation: Limiting Exposure
Segmentation restricts attacker movement.

Techniques include:
- Subnets
- VLANs
- Firewalls between network zones

Failure in one segment should not collapse the entire network.

---

## Rate Limiting and Traffic Filtering
Rate limiting assumes trust will be abused.

Benefits include:
- Reducing ICMP flooding impact
- Mitigating spoofed and reflection traffic
- Preserving availability under stress

Filtering malformed or unexpected packets further reduces exposure.

---

## Secure Routing and Anti-Spoofing Controls
Defensive routing measures include:
- Ingress and egress filtering
- Authenticated routing protocols (e.g., OSPF authentication)
- Rejecting invalid or unexpected routing updates

These controls reduce impersonation and routing manipulation.

---

## Logging and Monitoring
Logging accepts that failures will occur.

Effective monitoring focuses on:
- Abnormal ICMP behavior
- Unexpected routing changes
- Unusual ARP or IP patterns
- Traffic volume anomalies

Visibility turns silent failure into actionable signal.

---

## Key Insight
Network-layer defense is built on **managed distrust**.

Resilient systems expect failure and are designed to survive it.
