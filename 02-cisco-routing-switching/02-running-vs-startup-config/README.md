# LAB 02 – Running Configuration vs. Startup Configuration

**Category:** Cisco Routing & Switching  
**Topic:** Configuration Management  
**Platform:** Cisco IOS / PacketMentor  
**Device:** Cisco Router  
**Difficulty:** Beginner  
**Status:** Completed

---

## 1. Overview

This lab demonstrates the difference between the running configuration and startup configuration on a Cisco router.

It focuses on configuring a router interface, saving configuration changes to NVRAM, and ensuring that the configuration persists after a device reload.

## 2. Objectives

- Understand the difference between running-config and startup-config.
- Configure the router hostname.
- Configure and enable a GigabitEthernet interface.
- Assign an IPv4 address to the interface.
- Add an interface description.
- Save the running configuration to startup-config.
- Verify configuration persistence.

## 3. Lab Environment

| Parameter | Value |
|---|---|
| Device | Cisco Router |
| Initial Hostname | Router |
| Target Hostname | CORE-1 |
| Interface | GigabitEthernet0/0 |
| Configuration Storage | NVRAM |

## 4. Configuration Requirements

| Feature | Requirement |
|---|---|
| Hostname | CORE-1 |
| Interface | Gi0/0 |
| Interface Status | Enabled |
| IPv4 Address | Configured |
| Interface Description | Configured |
| Configuration Persistence | Saved to NVRAM |

## 5. Implementation

The lab covers the following configuration tasks:

### 5.1 Hostname Configuration

Rename the router from its default hostname to `CORE-1`.

### 5.2 Interface Configuration

Configure GigabitEthernet0/0 with:

- An IPv4 address and subnet mask.
- An interface description.
- The interface administrative state set to enabled.

### 5.3 Save Configuration

Persist the current running configuration to startup configuration in NVRAM.

## 6. Verification

Commands used to verify the configuration:

```text
show running-config
show startup-config
show ip interface brief
```

The verification should confirm:

- The hostname is `CORE-1`.
- GigabitEthernet0/0 has the configured IP address.
- The interface is administratively enabled.
- The saved startup configuration contains the intended changes.

## 7. Technical Explanation

### Running Configuration

- The active configuration currently used by the router.
- Stored in RAM.
- Changes take effect immediately.
- Changes can be lost after a reload or power cycle if they are not saved.

### Startup Configuration

- The configuration loaded when the device starts.
- Stored in NVRAM.
- Preserves saved configuration across reloads and power cycles.

### Key Difference

| Feature | Running-config | Startup-config |
|---|---|---|
| Storage | RAM | NVRAM |
| Active configuration | Yes | No |
| Survives reload | No, unless saved | Yes |
| Updated immediately | Yes | No |

## 8. Evidence

- [ ] Running configuration screenshot
- [ ] Startup configuration screenshot
- [ ] Interface status screenshot
- [ ] Saved configuration verification

_Add actual lab screenshots to the screenshots folder._

## 9. Key Learnings

- Understanding configuration storage on Cisco devices.
- Understanding why configuration changes must be saved.
- Configuring and enabling router interfaces.
- Verifying interface status and configuration persistence.
- Understanding the operational importance of NVRAM.

## 10. References

- Practice Platform: [PacketMentor](https://packetmentor.com/)
- Exercise: Configure and save: running-config vs. startup-config.

---

**Author:** Nguyen Van An
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
