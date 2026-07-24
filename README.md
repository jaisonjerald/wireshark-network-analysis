# DNS Protocol Analysis

## Objective

Capture and analyze DNS request and response packets using Wireshark to understand how domain names are resolved into IPv4 addresses.

### Lab Environment

- Kali Linux
- Oracle VirtualBox
- Wireshark
- NAT Network

### Display Filter

```text
dns
```

### Command Used

```bash
dig google.com
```

### DNS Capture

![DNS Query and Response](images/03-dns-analysis.png)

*Figure 3: DNS query and response captured using Wireshark.*

### Packet Analysis

#### DNS Query

| Field | Value |
|-------|-------|
| Source IP | 10.0.2.15 |
| Destination IP | 172.23.203.65 |
| Protocol | DNS |
| Transport | UDP |
| Destination Port | 53 |
| Query Type | A Record |
| Domain | google.com |

#### DNS Response

| Field | Value |
|-------|-------|
| Source IP | 172.23.203.65 |
| Destination IP | 10.0.2.15 |
| Response | google.com → 142.251.223.238 |

### Security Relevance

- DNS resolves domain names to IP addresses.
- DNS traffic can reveal malicious domains.
- SOC analysts monitor DNS for:
  - DNS tunneling
  - Command-and-Control (C2) communication
  - Malware beaconing
  - Suspicious domain lookups

### Key Takeaways

- DNS commonly uses **UDP port 53**.
- **A records** resolve hostnames to IPv4 addresses.
- Most web connections begin with a DNS lookup.
- Wireshark enables detailed analysis of DNS requests and responses.
