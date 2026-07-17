# Fallback AP Takeover

## Overview
Many IoT devices enter **fallback Wi-Fi AP mode** when RF interference or pairing failures occur.  
Attackers intentionally destabilize RF to force devices into insecure modes.

---

## Attack Flow (Conceptual)
1. Attacker introduces RF interference.
2. IoT device disconnects from Wi-Fi.
3. Device enters fallback AP mode (open Wi-Fi network).
4. Attacker connects to the device.
5. Attacker extracts Wi-Fi credentials or takes control.

---

## Why Fallback AP Modes Are Dangerous
- Often unsecured (open AP)
- Broadcast SSID reveals device type
- Device exposes configuration endpoints
- Wi-Fi credentials stored internally

---

## Detection Signals
- IoT device broadcasting new SSID
- Device resets during RF instability
- Unexpected pairing mode activation
- RF packet storms preceding AP activation

---

## Defensive Notes
- Disable fallback AP mode
- Enforce secure pairing
- Segment IoT networks
- Monitor RF interference patterns

**Related:** [IoT Threat Model](ca://s?q=Explain_pattern_driven_targeting)
