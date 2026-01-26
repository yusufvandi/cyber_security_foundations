# ARP Spoofing — Trust Abuse at Layer 2

Address Resolution Protocol (ARP) is a fundamental Layer 2 mechanism that enables devices on a local network to map IP addresses to MAC addresses.

ARP was designed for **simplicity and speed**, not security.  
As a result, it relies entirely on **implicit trust**, making it a common entry point for local network attacks.

---

## What ARP Does

ARP answers a simple question:

> “Which MAC address corresponds to this IP address?”

It operates using:
- Broadcast requests
- Stateless replies
- No authentication or verification

Any device on the local network can respond to an ARP request.

---

## Core Trust Assumptions in ARP

ARP assumes that:
- Devices respond honestly
- IP-to-MAC mappings are truthful
- Local networks are cooperative environments

These assumptions are not mistakes — they are **design trade-offs** made to ensure:
- Low latency
- Minimal overhead
- Broad compatibility

---

## How ARP Spoofing Works

In an ARP spoofing attack, an attacker sends **forged ARP replies** to one or more devices on the network.

The attacker claims:
- “I am the gateway”
- “I am the target host”

As a result:
- Traffic meant for legitimate devices is redirected to the attacker
- The attacker can observe, modify, or drop traffic

Importantly:
- No malformed packets are required
- No protocol rules are violated
- All communication remains valid ARP traffic

---

## Why ARP Spoofing Succeeds

ARP spoofing works because:
- ARP accepts unsolicited replies
- Devices update ARP tables automatically
- There is no mechanism to verify identity

The protocol prioritizes **availability and speed** over correctness.

The system behaves exactly as designed.

---

## Impact of ARP Spoofing

Once positioned between hosts, an attacker can:
- Perform Man-in-the-Middle (MitM) attacks
- Intercept credentials
- Downgrade or disrupt encrypted sessions
- Cause Denial of Service by dropping packets

Even encrypted traffic can be affected at this stage.

---

## Why “Secure Networks” Are Still Vulnerable

ARP spoofing occurs **inside** trusted environments:
- Corporate LANs
- University networks
- Data centers
- Home networks

Firewalls and perimeter defenses do not protect against it because:
- The attack originates internally
- The traffic appears legitimate
- Trust is assumed, not enforced

---

## Defensive Considerations

Defenses at Layer 2 focus on **reducing trust**, not eliminating attacks:

- Static ARP entries (limited scalability)
- ARP inspection on managed switches
- Network segmentation
- Monitoring for anomalous ARP behavior

No single defense is sufficient on its own.

---

## Key Insight

ARP spoofing succeeds not because ARP is broken, but because:

> **Trust without verification is exploitable.**

This same pattern reappears at higher layers, where trust becomes even more costly and more dangerous.

---

## Progression

This Layer 2 trust abuse establishes the foundation for later phases of this project:
- Transport-layer trust exhaustion (Week 2)
- Application-layer logic abuse
- Encryption misconceptions
- Resilience-focused defense design
