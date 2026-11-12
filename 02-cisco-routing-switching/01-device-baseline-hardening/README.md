# LAB 01 – Cisco Device Baseline & Hardening

<p align="center">
  <strong>Network Engineering | Cisco IOS | Device Security</strong>
</p>

## 1. Overview

This lab focuses on establishing a basic configuration baseline and applying initial security settings to a fresh Cisco router.

**Lab Platform:** PacketMentor  
**Device:** Cisco Router  
**Hostname:** EDGE-1  
**Difficulty:** Beginner  
**Category:** Network Administration & Security

## 2. Objectives

The objectives of this lab are:

- Configure a meaningful device hostname.
- Set an enable secret for privileged EXEC access.
- Protect console access with a password.
- Protect VTY lines for remote terminal access.
- Enable password encryption in the configuration.
- Verify the final configuration using `show running-config`.

## 3. Initial Device State

| Parameter | Initial Value |
|---|---|
| Hostname | Router |
| Device State | Fresh / Default Configuration |
| Security Configuration | Default |

## 4. Configuration Requirements

| Feature | Target Configuration |
|---|---|
| Hostname | EDGE-1 |
| Enable Secret | Configured |
| Console Line | Password Protected |
| VTY Lines | Password Protected |
| Password Encryption | Enabled |

**Security note:** Actual passwords and secrets are intentionally excluded from this public repository.

## 5. Implementation

The device baseline configuration covers the following areas:

### 5.1 Hostname Configuration

Rename the default device hostname to `EDGE-1`.

### 5.2 Privileged EXEC Security

Configure an enable secret to protect privileged EXEC mode.

### 5.3 Console Access Protection

Configure password protection for the physical console line.

### 5.4 VTY Access Protection

Configure password protection for virtual terminal lines used for remote access.

### 5.5 Password Encryption

Enable `service password-encryption` to prevent line passwords from appearing as readable clear text in the configuration.

## 6. Verification

Verification command:

```text
show running-config
```

The final configuration should confirm:

- Hostname is set to EDGE-1.
- Enable secret is configured.
- Console line has password protection.
- VTY lines have password protection.
- Password encryption service is enabled.

**Verification result:** Pending actual lab evidence.

## 7. Security Considerations

- `enable secret` is preferable to the legacy `enable password`.
- `service password-encryption` provides only weak Type 7 obfuscation for line passwords; it is not strong encryption.
- Passwords and secrets must never be published in a public repository.
- For production environments, use stronger authentication controls such as SSH and centralized AAA where supported.

## 8. Evidence

Screenshots will be added after completing the lab:

- [ ] Final hostname verification
- [ ] Enable secret configuration (redacted)
- [ ] Console and VTY configuration (passwords redacted)
- [ ] Password encryption verification
- [ ] Sanitized `show running-config` output

## 9. Learning Outcomes

To be updated after completing the lab:

- Understanding Cisco device baseline configuration.
- Understanding the difference between privileged EXEC and line access protection.
- Understanding the purpose and limitations of password encryption.
- Learning how to verify router configuration.

## 10. Reference

- Practice Platform: [PacketMentor](https://packetmentor.com/)
- Exercise: Device baseline: hostname, secret, console + VTY, encryption.

---

**Author:** Nguyen Van An
**Role:** Aspiring Network Engineer  
**Portfolio:** Network Engineering Portfolio
