# LAB 01 – Basic LAN Configuration

> **Category:** Networking Fundamentals  
> **Level:** Beginner  
> **Platform:** Cisco Packet Tracer  
> **Status:** In Progress

---

## 1. Objective

The objective of this lab is to understand how devices communicate within a Local Area Network (LAN).

After completing this lab, I should be able to:

- Understand basic LAN architecture.
- Connect PCs using an Ethernet switch.
- Configure IPv4 addresses manually.
- Test connectivity using ICMP Ping.
- Inspect the switch MAC Address Table.
- Identify and troubleshoot basic network connectivity issues.

## 2. Network Topology

**Network diagram:**

_Add topology screenshot here._

## 3. Network Devices

| Device | Model | Quantity |
|---|---|---:|
| Switch | Cisco 2960 | 1 |
| PC | PC-PT | 2 |
| Cable | Copper Straight-Through | 2 |

## 4. IP Addressing Plan

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| PC-A | FastEthernet0 | 192.168.1.10 | 255.255.255.0 |
| PC-B | FastEthernet0 | 192.168.1.20 | 255.255.255.0 |

**Network:** 192.168.1.0/24

**Default Gateway:** Not required for communication within this same subnet.

## 5. Implementation

### Step 1 – Physical Connection

- Connect PC-A to SW1 using FastEthernet0/1.
- Connect PC-B to SW1 using FastEthernet0/2.
- Use Copper Straight-Through cables.

### Step 2 – Configure IPv4

Configure the IP address and subnet mask on both PCs according to the IP addressing plan.

### Step 3 – Verify Connectivity

From PC-A, execute:

```bash
ping 192.168.1.20
```

**Ping result:** _To be updated after testing._

_Add ping screenshot here._

### Step 4 – Verify MAC Address Table

On SW1, execute:

```text
enable
show mac address-table
```

**Observation:** _To be updated after testing._

_Add MAC address table screenshot here._

## 6. Troubleshooting

### Test Case 1 – Incorrect IP Subnet

Change PC-B IP address to:

```text
192.168.2.20
```

Run the ping test again.

**Expected observation:** PC-A and PC-B cannot communicate directly because they are in different IP subnets and no router is configured.

**Solution:** Restore PC-B IP address to 192.168.1.20.

## 7. Results

_To be completed after all tests are successful._

| Test | Expected Result | Actual Result |
|---|---|---|
| PC-A to PC-B Ping | Successful | Pending |
| MAC Address Learning | MAC entries visible | Pending |
| Incorrect IP Test | Connectivity fails | Pending |
| Restore Correct IP | Successful | Pending |

## 8. Key Takeaways

_To be completed after finishing the lab._

- What is a LAN?
- What is the role of a Layer 2 switch?
- What is the difference between IP and MAC addresses?
- Why can two devices in the same subnet communicate without a default gateway?
- What happens when two devices belong to different subnets without a router?

## 9. Evidence

- [ ] Network topology screenshot
- [ ] Successful Ping screenshot
- [ ] MAC Address Table screenshot
- [ ] Troubleshooting screenshot

---

**Author:** Nguyen Van An
**Project:** Network Engineering Portfolio
