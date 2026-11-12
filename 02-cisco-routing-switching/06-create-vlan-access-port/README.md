# LAB 06 – Create a VLAN and Assign an Access Port

## Overview

| Field | Details |
|---|---|
| Category | Cisco Switching |
| Platform | PacketMentor |
| Device | Cisco Catalyst 2960 |
| Switch | SW1 |
| Interface | FastEthernet 0/1 |
| VLAN ID | 10 |
| VLAN Name | Engineering |
| Difficulty | Beginner |
| Status | Completed |

## Objectives

- Create VLAN 10 and name it `Engineering`.
- Configure `Fa0/1` as an access port.
- Assign `Fa0/1` to VLAN 10.
- Verify VLAN membership using `show vlan brief`.

## Network Requirements

| Component | Configuration |
|---|---|
| Switch | SW1 |
| Switch Model | Cisco 2960 |
| VLAN ID | 10 |
| VLAN Name | Engineering |
| Interface | Fa0/1 |
| Port Mode | Access |
| Assigned VLAN | VLAN 10 |

## Implementation Summary

The lab focuses on basic Layer 2 switching configuration:

1. Created VLAN 10 with the name `Engineering`.
2. Configured FastEthernet 0/1 as an access port.
3. Assigned the access port to VLAN 10.
4. Verified VLAN creation and port assignment.

## Verification

The following command was used to verify the configuration:

```bash
show vlan brief
```

Expected verification:

- VLAN 10 exists.
- VLAN 10 is named `Engineering`.
- FastEthernet 0/1 appears under VLAN 10.
- VLAN 1 no longer lists Fa0/1.

## Technical Explanation

### What is a VLAN?

A Virtual Local Area Network (VLAN) logically separates a physical Layer 2 network into multiple broadcast domains.

VLANs help improve:

- Network segmentation.
- Broadcast traffic management.
- Security and access control.
- Network administration.

### What is an Access Port?

An access port belongs to a single VLAN and is typically used to connect end devices such as computers, printers, and workstations.

In this lab, `Fa0/1` is assigned to VLAN 10 (`Engineering`).

## Key Learning Outcomes

- Understanding VLAN fundamentals.
- Creating and naming VLANs on Cisco switches.
- Configuring access ports.
- Assigning switch interfaces to VLANs.
- Verifying VLAN membership.

## Evidence

Screenshots are stored in the `screenshots/` directory.

- [x] VLAN 10 creation and naming.
- [x] Fa0/1 access port assignment.
- [x] VLAN membership verification.

## Practice Source

- Platform: PacketMentor
- Exercise: Create a VLAN, assign an access port.

---

**Author:** Hoan Van  
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
