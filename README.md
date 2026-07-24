# Wireshark Network Analysis

This repository demonstrates practical packet analysis using **Wireshark** in a virtual lab environment. The project covers fundamental networking protocols and explains their role in cybersecurity investigations.

---

## Lab Environment

- **Operating System:** Kali Linux
- **Virtualization:** Oracle VirtualBox
- **Tool:** Wireshark
- **Network Modes:** NAT & Host-Only Adapter

---

# 1. ARP Protocol Analysis

![ARP Analysis](images/01-arp-analysis.png)

*Figure 1: ARP Request and ARP Reply captured using Wireshark.*

> *(Paste your ARP analysis here.)*

---

# 2. ICMP Protocol Analysis

![ICMP Analysis](images/02-icmp-analysis.png)

*Figure 2: ICMP Echo Request and Echo Reply captured using Wireshark.*

> *(Paste your ICMP analysis here.)*

---

# 3. DNS Protocol Analysis

## Objective

Capture and analyze DNS request and response packets using Wireshark to understand how domain names are resolved into IPv4 addresses.

### Display Filter

```text
dns
```

### Command Used

```bash
dig google.com
```

### DNS Capture

![DNS Analysis](images/03-dns-analysis.png)

*Figure 3: DNS query and response captured using Wireshark.*

### Packet Analysis

| Field | Value |
|-------|-------|
| Source IP | 10.0.2.15 |
| Destination IP | 172.23.203.65 |
| Protocol | DNS |
| Transport | UDP |
| Destination Port | 53 |
| Query Type | A Record |
| Domain | google.com |

### DNS Response

| Field | Value |
|-------|-------|
| Source IP | 172.23.203.65 |
| Destination IP | 10.0.2.15 |
| Response | google.com → 142.251.223.238 |

### Security Relevance

- Detect malicious domains
- DNS tunneling detection
- Command-and-Control (C2) communication
- Malware beaconing
- Threat hunting

---

## Skills Demonstrated

- Wireshark Packet Analysis
- Network Troubleshooting
- DNS Analysis
- ICMP Analysis
- ARP Analysis
- Network Traffic Inspection
- Security Monitoring

---

## Conclusion

This project demonstrates hands-on experience capturing and analyzing common network protocols using Wireshark. Understanding ARP, ICMP, and DNS traffic is fundamental for network troubleshooting, threat hunting, malware analysis, and Security Operations Center (SOC) investigations.
