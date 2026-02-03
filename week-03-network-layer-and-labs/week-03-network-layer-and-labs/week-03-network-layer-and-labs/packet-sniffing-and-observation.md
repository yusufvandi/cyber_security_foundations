# Packet Sniffing and Network Observation Lab

## Environment
- Operating System: Windows 10
- Network: Wi-Fi via mobile hotspot
- Tool: Wireshark

---

## Objective
Observe network-layer and transport-layer behavior during normal system activity and ICMP-based diagnostics.

The goal was to understand:
- What is visible to an endpoint
- What is hidden by network infrastructure
- How trust and visibility differ in practice

---

## Method
- Wireshark capture started on the active Wi-Fi interface
- ICMP traffic generated using standard `ping` commands
- IPv4 (`icmp`) and IPv6 (`icmpv6`) display filters applied
- Traffic observed both with and without filters

---

## Observations
- TCP traffic was clearly visible
- TLS-encrypted traffic was present but unreadable
- No ICMP or ICMPv6 packets were observed
- Packet capture functioned correctly, confirming active traffic flow

---

## Analysis
The absence of ICMP traffic indicates that the mobile hotspot network:
- Filters or proxies control-plane protocols
- Abstracts diagnostic traffic from the end host
- Suppresses visibility without notifying the user

Application connectivity remained functional despite this loss of observability.

---

## Key Insight
Encryption hides content — **not behavior**.

Network intermediaries can silently enforce policy while maintaining usability, creating blind spots for defenders.

Availability without visibility is a security risk.
