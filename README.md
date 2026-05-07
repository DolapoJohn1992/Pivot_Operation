# Operation Pivot: Redis Service Discovery

## Overview
This project documents the successful execution of a network pivot to discover internal services within a segmented lab environment.

## Technical Execution
- **Initial Access:** Established a foothold on the gateway at `172.50.0.10` using Metasploit's SSH login module.
- **Pivoting:** Configured an internal route to the `10.0.9.0/24` subnet.
- **Proxy Configuration:** Deployed a SOCKS4a proxy server to bridge external tools with the internal network.
- **Discovery:** Utilized `proxychains4` and `nmap` to identify an open Redis service (Port 6379) on the internal host `10.0.9.50`.

## Artifacts
- `pivot_success.png`: Screenshot verifying the open Redis port via the established tunnel.
