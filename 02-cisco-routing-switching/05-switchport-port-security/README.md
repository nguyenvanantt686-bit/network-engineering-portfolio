# LAB 05 – Harden a Switchport with Port Security

**Category:** Cisco Switching & Security  
**Topic:** Layer 2 Port Security  
**Platform:** PacketMentor  
**Device:** Cisco Catalyst Switch (SW1)  
**Interface:** FastEthernet0/1  
**Difficulty:** Beginner  
**Status:** Completed

---

## 1. Overview

This lab focuses on securing a Cisco switch access port using Port Security.

The configuration restricts the number of MAC addresses allowed on the port, dynamically learns the permitted MAC address through sticky learning, and shuts down the port when a security violation occurs.

## 2. Objectives

- Configure an access port in VLAN 10.
- Enable Port Security on the switchport.
- Restrict the port to one MAC address.
- Enable sticky MAC address learning.
- Configure the violation action to shutdown.
- Verify the Port Security configuration and status.

## 3. Lab Environment

| Parameter | Value |
|---|---|
| Switch | SW1 |
| Interface | FastEthernet0/1 |
| VLAN | 10 |
| Port Mode | Access |
| Maximum MAC Addresses | 1 |
| MAC Learning | Sticky |
| Violation Mode | Shutdown |

## 4. Configuration Requirements

| Feature | Required Configuration |
|---|---|
| VLAN Assignment | VLAN 10 |
| Switchport Mode | Access |
| Port Security | Enabled |
| Maximum MAC | 1 |
| Sticky Learning | Enabled |
| Violation Action | Shutdown |

## 5. Implementation

The lab covers the following configuration tasks:

### 5.1 Access Port Configuration

Configure Fa0/1 as an access port assigned to VLAN 10.

### 5.2 Port Security Configuration

Enable Port Security on Fa0/1 and restrict the interface to a maximum of one secure MAC address.

### 5.3 Sticky MAC Learning

Enable sticky learning so the switch dynamically learns the connected device's MAC address and adds it to the running configuration.

### 5.4 Violation Handling

Configure the violation mode to shutdown, causing the interface to enter the error-disabled state when a Port Security violation occurs.

## 6. Verification

Commands used to verify the configuration:

```text
show running-config interface fastEthernet 0/1
show port-security interface fastEthernet 0/1
show port-security address
show vlan brief
```

Expected results:

- Fa0/1 is assigned to VLAN 10.
- Port Security is enabled.
- Maximum secure MAC addresses is 1.
- Sticky MAC learning is enabled.
- Violation mode is Shutdown.

## 7. Technical Explanation

### Port Security

A Layer 2 security feature that restricts which MAC addresses can send traffic through a switchport.

### Maximum MAC Address

Limits the number of secure MAC addresses permitted on the interface. In this lab, only one MAC address is allowed.

### Sticky MAC Learning

Dynamically learns MAC addresses and adds them to the running configuration as secure sticky entries.

### Shutdown Violation Mode

When a violation occurs, the switch places the interface into the error-disabled state and generates a security violation event.

## 8. Evidence

- [ ] Access port and VLAN configuration
- [ ] Port Security configuration
- [ ] Sticky MAC address entry
- [ ] Port Security verification output
- [ ] Violation test result (if performed)

## 9. Key Learnings

- Understanding Layer 2 switchport security.
- Restricting MAC addresses on an access port.
- Using sticky MAC learning.
- Understanding Port Security violation modes.
- Verifying and troubleshooting secure switchports.

## 10. References

- Practice Platform: [PacketMentor](https://packetmentor.com/)
- Exercise: Harden a switchport with port-security.

---

**Author:** Hoan Van  
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
