# Transport Layer Trust and State

## Role of the Transport Layer
The Transport Layer (Layer 4) provides end-to-end communication between applications.
Its responsibilities include:
- Reliable data delivery
- Flow control
- Congestion control
- Connection management

Unlike lower layers, the transport layer introduces **state**.

## What State Means
State includes:
- Connection tracking
- Sequence numbers
- Buffers for retransmission
- Timers and retransmission logic

This state allows systems to recover from packet loss and deliver ordered data.
However, state must be **allocated and maintained over time**.

## Trust Implications of State
To function efficiently, the transport layer assumes:
- Endpoints will cooperate
- Connections will be completed
- Resources allocated early will be used honestly

State is created **before intent is verified**.
This introduces asymmetric cost:
- Creating a request is cheap
- Holding state is expensive

## Key Insight
Reliability at the transport layer is achieved through trusted cooperation.
That trust improves performance — and creates an attack surface when abused.
