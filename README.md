# Configuration Management

## Routing
### Firewall

| Protocol | Source IP | Source Port | Dest IP | Dest Port | Action
| -------- | ------- | ------- | ------- | ------- | ------- |
| TCP | - | - | - | 20-21 | Reject |
| TCP | - | - | - | 23 | Reject |
| TCP | - | - | - | 25 | Reject |
| UDP | - | - | - | 69 | reject |
| UDP/TCP | - | - | - | 135 | reject |
| UDP/TCP | - | - | - | 137-139 | reject |
| UDP | - | - | - | 161-162 | reject |
| TCP | - | - | - | 445 | reject |
| UDP | - | - | - | 514 | reject
