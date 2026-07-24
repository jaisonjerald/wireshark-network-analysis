# DNS Protocol Analysis

## Objective
Capture and analyze DNS request and response packets using Wireshark.

## Lab Environment

- Kali Linux
- VirtualBox
- NAT Network
- Wireshark

## Display Filter

```text
dns
```

## Command Used

```bash
dig google.com
```

## Observations

### DNS Query
- Source IP: 10.0.2.15
- Destination IP: 172.23.203.65
- Query Type: A Record
- Domain: google.com

### DNS Response
- Source IP: 172.23.203.65
- Destination IP: 10.0.2.15
- Returned IPv4 Address: 142.251.223.238

## Security Analysis

DNS is responsible for translating domain names into IP addresses.

SOC analysts inspect DNS traffic to:
- Detect malicious domains
- Identify DNS tunneling
- Investigate malware communications
- Detect command-and-control (C2) traffic

## Key Learning

- DNS uses UDP port 53 by default.
- A records resolve hostnames to IPv4 addresses.
- Every web request usually begins with a DNS lookup.
