# Configuration Management
A set of configuration options and notes for future reference.

## Routing

### Firewall
> [!NOTE]
> Outgoing Traffic: `Accept`
> Incoming Traffic: `Drop`

| Name      | Protocol | Source IP | Source Port | Dest IP | Dest Port | Action |
| --------- | -------- | --------- | ----------- | ------- | --------- | ------ |
| ftp       | TCP      | -         | -           | -       | 20-21     | Drop   |
| telnet    | TCP      | -         | -           | -       | 23        | Drop   |
| smtp      | TCP      | -         | -           | -       | 25        | Drop   |
| tftp      | UDP      | -         | -           | -       | 69        | Drop   |
| msrpc     | UDP/TCP  | -         | -           | -       | 135       | Drop   |
| netbiosip | UDP/TCP  | -         | -           | -       | 137-139   | Drop   |
| snmp      | UDP      | -         | -           | -       | 161-162   | Drop   |
| smbip     | TCP      | -         | -           | -       | 445       | Drop   |
| syslog    | UDP      | -         | -           | -       | 514       | Drop   |

