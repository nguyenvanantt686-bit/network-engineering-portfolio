# LAB 04 – IPv6 Basics: Address an Interface

**Category:** Cisco Routing & Switching  
**Topic:** IPv6 Addressing  
**Platform:** PacketMentor  
**Device:** Cisco Router (R1)  
**Difficulty:** Beginner  
**Status:** Completed

---

## 1. Overview

This lab introduces basic IPv6 configuration on a Cisco router.

The objective is to enable IPv6 routing globally and configure a Global Unicast IPv6 address on the GigabitEthernet0/0 interface.

## 2. Objectives

- Understand basic IPv6 addressing.
- Enable IPv6 routing globally on the router.
- Configure a Global Unicast IPv6 address.
- Enable the router interface.
- Verify the IPv6 interface configuration.

## 3. Lab Environment

| Parameter | Value |
|---|---|
| Device | Cisco Router |
| Hostname | R1 |
| Interface | GigabitEthernet0/0 |
| IPv6 Address | 2001:db8::1/64 |
| Address Type | Global Unicast |
| Prefix Length | /64 |

## 4. Configuration Requirements

| Configuration | Required Value |
|---|---|
| IPv6 Routing | Enabled globally |
| Interface | Gi0/0 |
| IPv6 Address | 2001:db8::1/64 |
| Interface Status | Enabled |

## 5. Implementation

The lab covers two main configuration tasks:

### 5.1 Enable IPv6 Routing

Enable IPv6 unicast routing globally on R1.

### 5.2 Configure the Interface

Assign the IPv6 Global Unicast address `2001:db8::1/64` to GigabitEthernet0/0 and enable the interface.

## 6. Verification

Commands used to verify the configuration:

```text
show running-config
show ipv6 interface brief
show ipv6 interface gigabitEthernet 0/0
```

Expected results:

- IPv6 unicast routing is enabled.
- Gi0/0 has the Global Unicast address `2001:db8::1/64`.
- Gi0/0 is administratively enabled.
- Interface operational status is verified.

## 7. Technical Explanation

### IPv6 Unicast Routing

IPv6 routing must be enabled globally before a Cisco router can forward IPv6 packets between interfaces.

### Global Unicast Address

A Global Unicast Address is an IPv6 address intended for communication beyond the local network.

### Prefix Length /64

The `/64` prefix identifies the network portion of the IPv6 address and is commonly used in LAN networks.

### Documentation Prefix

The prefix `2001:db8::/32` is reserved for documentation and examples. It is not intended for public Internet routing.

## 8. Evidence

- [ ] Global IPv6 routing configuration
- [ ] IPv6 interface address configuration
- [ ] `show ipv6 interface brief` output
- [ ] PacketMentor lab completion screenshot

## 9. Key Learnings

- Understanding IPv6 Global Unicast addressing.
- Enabling IPv6 routing on Cisco routers.
- Assigning IPv6 addresses to router interfaces.
- Understanding IPv6 prefix lengths.
- Verifying IPv6 interface configuration.

## 10. References

- Practice Platform: [PacketMentor](https://packetmentor.com/)
- Exercise: IPv6 basics: address an interface.

---

**Author:** Hoan Van  
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
