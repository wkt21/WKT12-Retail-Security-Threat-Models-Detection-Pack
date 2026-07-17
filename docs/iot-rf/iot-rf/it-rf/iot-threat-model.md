# IoT Threat Model (Retail & Consumer Environments)

## Overview
IoT devices in retail and home environments operate heavily in the 2.4GHz band.  
They rely on BLE, Zigbee, Wi-Fi, and proprietary RF protocols — many of which lack authentication or fallback securely.

Attackers exploit:
- Broadcast protocols
- Weak pairing flows
- RF interference
- Fallback AP modes
- Predictable device behavior

---

## IoT Attack Classes (Conceptual Only)

### 1. Broadcast Command Injection
Injecting fake commands into BLE/Zigbee broadcast channels.

### 2. Pairing Exploitation
Hijacking insecure pairing flows to steal credentials or take control.

### 3. Fallback AP Takeover
Triggering RF instability to force devices into open Wi-Fi AP mode.

### 4. RF Replay Attacks
Replaying previously captured RF commands (unlock, on/off, pairing).

### 5. IoT → Wi-Fi Pivot
Using compromised IoT devices to access Wi-Fi credentials stored internally.

---

## Why IoT Is Vulnerable
- Broadcast-based communication
- Weak or unauthenticated pairing
- Insecure fallback modes
- No RF spectrum monitoring
- Predictable device resets

---

## Defensive Notes
- Enforce secure pairing
- Disable fallback AP modes
- Segment IoT networks
- Monitor RF anomalies

**Related:** [RF Spectrum Monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
