# Packet Sniffing and Transport Layer Observation Lab

## Environment
- Operating System: Windows 10
- Network: Wi-Fi via mobile hotspot
- Tool: Wireshark

## Objective
Observe how the transport layer establishes, maintains, and terminates state during normal application activity.

## Method
- Wireshark capture initiated on active Wi-Fi interface
- Display filters applied for TCP traffic
- Normal web browsing activity generated via browser
- No attack traffic introduced

## Observations
- TCP handshake packets (SYN, SYN-ACK, ACK) observed prior to data exchange
- Application data transmitted only after handshake completion
- Payloads were encrypted and unreadable
- Connection teardown involved FIN and ACK packets
- Multiple concurrent TCP connections were active simultaneously

## Analysis
The capture confirms that:
- State is established before application data is exchanged
- Resources are committed early in the communication lifecycle
- Encryption protects content but not connection behavior
- Connection management relies on cooperation rather than verification

This demonstrates that availability depends on how well state is managed under load.

## Key Insight
The transport layer enforces reliability by allocating memory and time.
These same mechanisms become liabilities when trust is abused at scale.
