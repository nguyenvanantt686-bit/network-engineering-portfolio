# LAB 03 – Assign an IP to a Router Interface

**Category:** Cisco Routing & Switching  
**Topic:** Router Interface Configuration  
**Platform:** PacketMentor  
**Device:** Cisco Router (R1)  
**Difficulty:** Beginner  
**Status:** Completed

---

## 1. Overview

This lab focuses on configuring IPv4 addresses and descriptions on Cisco router interfaces, enabling the interfaces, and verifying their operational status.

The router uses two GigabitEthernet interfaces to connect separate network segments: an internal LAN and a DMZ network.

## 2. Objectives

- Configure IPv4 addresses on router interfaces.
- Assign descriptions to interfaces.
- Enable administratively shut interfaces.
- Verify interface IP addresses and operational status.
- Understand the role of router interfaces in connecting different networks.

## 3. Lab Topology

| Device | Interface | Network | IP Address |
|---|---|---|---|
| R1 | Gi0/0 | LAN-INSIDE | 10.0.0.1/24 |
| R1 | Gi0/1 | LAN-DMZ | 192.168.1.1/24 |

## 4. Configuration Requirements

| Interface | IP Address | Description | Status |
|---|---|---|---|
| Gi0/0 | 10.0.0.1/24 | LAN-INSIDE | Enabled |
| Gi0/1 | 192.168.1.1/24 | LAN-DMZ | Enabled |

## 5. Implementation

The lab covers:

- Configuring GigabitEthernet0/0 with an IPv4 address and interface description.
- Configuring GigabitEthernet0/1 with an IPv4 address and interface description.
- Enabling both interfaces.
- Verifying the interface configuration.

## 6. Verification

Verification command:

```text
show ip interface brief
```

Expected results:

- Gi0/0 has IP address `10.0.0.1`.
- Gi0/1 has IP address `192.168.1.1`.
- Both interfaces show `up/up` when connected to active links.
- Both interfaces are administratively enabled.

## 7. Technical Explanation

### Interface IP Address

A router interface IP address identifies the router within a specific IP network and can serve as the default gateway for devices in that network.

### Interface Description

Descriptions help administrators identify the purpose of each interface and make network troubleshooting easier.

### Interface Status

- **Administratively down:** The interface has been disabled using the shutdown command.
- **Up/Up:** The interface and its line protocol are operational.
- **Up/Down:** The physical interface is up, but the line protocol is not operational.

## 8. Evidence

- [ ] Router interface configuration
- [ ] `show ip interface brief` output
- [ ] PacketMentor lab completion screenshot

## 9. Key Learnings

- Assigning IPv4 addresses to Cisco router interfaces.
- Configuring interface descriptions.
- Enabling router interfaces.
- Understanding interface operational states.
- Verifying router interface configurations.

## 10. References

- Practice Platform: [PacketMentor](https://packetmentor.com/)
- Exercise: Assign an IP to a router interface.

---

**Author:** Nguyen Van An 
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
