# IoT + RF Correlation Guide

## Overview
IoT and RF attacks often occur together.  
Correlating anomalies across BLE, Zigbee, Wi-Fi, RFID, and ESL systems reveals multi-vector attacks.

---

## Correlation Patterns

### 1. RF Interference → IoT Reset → Fallback AP
Signals:
- Packet storms
- Device resets
- Open AP mode

---

### 2. ESL Spoofing → RF Packet Flooding
Signals:
- ESL updates outside schedule
- 2.4GHz flooding
- Price changes across shelves

---

### 3. BLE/Zigbee Hijacking → POS Workflow Anomalies
Signals:
- Broadcast pairing attempts
- Unexpected automation triggers
- POS discount anomalies

---

### 4. RFID Tampering → IoT Alerts
Signals:
- Oversized EPC reads
- IoT sensor anomalies
- RF bursts near inventory areas

---

### 5. IoT Credential Theft → Wi-Fi Pivot
Signals:
- Fallback AP activation
- IoT device compromise
- Wi-Fi credential extraction

---

## SOC Action
- Prioritize multi-vector incidents
- Trigger containment workflows
- Deploy RF + IoT honeytokens
- Update RF monitoring rules

**Related:**  
- **[Incident Response](ca://s?q=Build_incident_response_docs)**  
- **[Hardening Checklist](ca://s?q=Build_hardening_docs)**
