# Configuration Management
A set of configuration options and notes for future reference.

## Routing

### Firewall

> [!NOTE]
> Outgoing Traffic: `Accept`
> Incoming Traffic: `Drop`

#### IPv4
| Name        | Protocol | Source IP | Source Port | Dest IP | Dest Port | Action |
| ----------- | -------- | --------- | ----------- | ------- | --------- | ------ |
| dns-allow-1 | UDP/TCP  | $DNS01    | -           | -       | 53        | Accept |
| dns-allow-2 | UDP/TCP  | $DNS02    | -           | -       | 53        | Accept |
| dns         | UDP/TCP  | -         | -           | -       | 53        | Drop   |
| smtp        | TCP      | -         | -           | -       | 25        | Drop   |
| telnet      | TCP      | -         | -           | -       | 23        | Drop   |
| tftp        | UDP      | -         | -           | -       | 69        | Drop   |
| ftp         | TCP      | -         | -           | -       | 20-21     | Drop   |
| snmp        | UDP      | -         | -           | -       | 161-162   | Drop   |
| msrpc       | UDP/TCP  | -         | -           | -       | 135       | Drop   |
| smbip       | TCP      | -         | -           | -       | 445       | Drop   |
| netbiosip   | UDP/TCP  | -         | -           | -       | 137-139   | Drop   |
| syslog      | UDP      | -         | -           | -       | 514       | Drop   |

#### IPv6
| Name        | Protocol | Source IP | Source Port | Dest IP | Dest Port | Action |
| ----------- | -------- | --------- | ----------- | ------- | --------- | ------ |
| dns-allow-1 | UDP/TCP  | $DNS01    | -           | -       | 53        | Accept |
| dns-allow-2 | UDP/TCP  | $DNS02    | -           | -       | 53        | Accept |
| dns         | UDP/TCP  | -         | -           | -       | 53        | Drop   |
| ftp         | TCP      | -         | -           | -       | 20-21     | Drop   |
| telnet      | TCP      | -         | -           | -       | 23        | Drop   |
| smtp        | TCP      | -         | -           | -       | 25        | Drop   |
| netbiosip   | UDP/TCP  | -         | -           | -       | 137-139   | Drop   |
| msrpc       | UDP/TCP  | -         | -           | -       | 135       | Drop   |
| tftp        | UDP      | -         | -           | -       | 69        | Drop   |
| snmp        | UDP      | -         | -           | -       | 161-162   | Drop   |
| smbip       | TCP      | -         | -           | -       | 445       | Drop   |
| syslog      | UDP      | -         | -           | -       | 514       | Drop   |

### Port Forwarding

| Service   | Protocol | Dest IP        | Dest Port | Src IP | Src Port  |
| --------- | -------- | -------------- | --------- | ------ | --------- |
| HTTPS     | UDP/TCP  | $HTTP_SRV      | 44301     | -      | 443       |
| iperf     | UDP/TCP  | $IPERF_SRV     | 5201-5202 | -      | 5201-5202 |
| Wireguard | UDP      | $WIREGUARD_SRV | 51820     | -      | 51820     |
| SFTP      | UDP/TCP  | $SFTP_SRV      | 2022      | -      | 2022      |
