# IoT Broadcast Hijacking

## Overview
Many IoT devices use broadcast packets (BLE, Zigbee, proprietary RF).  
Attackers inject fake commands or pairing requests into these channels.

---

## Attack Classes (Conceptual Only)

### 1. BLE Command Injection
Injecting:
- On/off commands
- Pairing requests
- Sensor triggers

### 2. Zigbee Broadcast Spoofing
Injecting:
- Fake automation events
- Device join requests
- Network key requests

### 3. ESL Broadcast Hijacking
Injecting:
- Fake price updates
- Rogue ESL pairing signals

---

## Why Broadcast Hijacking Works
- No mutual authentication
- Broadcast channels are open
- Devices trust pairing requests
- RF congestion hides malicious packets

---

## Detection Signals
- Unknown BLE/Zigbee device IDs
- Repeated pairing attempts
- ESL updates outside schedule
- RF packet storms

---

## Defensive Notes
- Enforce signed broadcast packets
- Require authenticated pairing
- Monitor BLE/Zigbee channels
- Deploy RF honeytokens

**Related:** [Pattern-Driven Targeting](ca://s?q=Explain_pattern_driven_targeting)
