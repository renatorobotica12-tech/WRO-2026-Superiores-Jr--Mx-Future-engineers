```mermaid
flowchart LR
    A[HuskyLens Camera] -->|Vision Data| B[Arduino Nano]
    B -->|Processed Data| C[EV3 Controller]
    C -->|Steering Control| D[Steering Motor]
    C -->|Speed Control| E[Drive Motor]
```
---
