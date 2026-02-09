# TCP Handshake and Resource Cost

## The TCP Three-Way Handshake
TCP establishes a connection using:
1. SYN — Client requests a connection
2. SYN-ACK — Server acknowledges and allocates resources
3. ACK — Client confirms and data transfer begins

Only after this exchange does application data flow.

## Design Assumptions
The handshake assumes:
- The client intends to complete the connection
- The client is reachable
- The request is legitimate

These assumptions are deliberate design choices made to support:
- Fast connection setup
- Scalability
- Compatibility across the global internet

## Asymmetric Resource Cost
The cost of sending a SYN packet is minimal.
The cost of responding includes:
- Memory allocation
- Connection table entries
- Timers and retransmission logic

The server commits resources **before** verifying intent.

## Key Insight
TCP is not weak.
It is optimized for cooperation — and that optimization creates exploitable asymmetry when cooperation is abused.
