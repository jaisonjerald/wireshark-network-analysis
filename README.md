# wireshark-network-analysis
Packet capture and network traffic analysis using Wireshark in a Windows 11 and Kali Linux lab environment.
# ARP Analysis

## Objective

Analyze the Address Resolution Protocol (ARP) exchange between Kali Linux and a Windows 11 virtual machine.

---

## Display Filter

```text
arp
```

---

## Observations

### ARP Request

```
Who has 192.168.56.101?
Tell 192.168.56.102
```

The Kali Linux VM broadcast an ARP Request to discover the MAC address associated with the target Windows 11 IP address.

---

### ARP Reply

```
192.168.56.101 is at 08:00:27:77:19:cf
```

The Windows 11 VM responded with its MAC address, allowing Kali Linux to update its ARP cache and communicate directly at Layer 2.

---

## Key Learning

- ARP resolves IPv4 addresses to MAC addresses.
- ARP Requests are broadcast.
- ARP Replies are unicast.
- ARP is required before IPv4 communication on a local network.
