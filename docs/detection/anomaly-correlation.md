# Anomaly Correlation Guide

## Purpose
Correlate POS, SCO, RFID, ESL, and RF anomalies to identify multi-vector retail attacks.

## Correlation Patterns

### 1. HID Injection + POS Workflow Escape
Signals:
- Fast scan cadence
- Unexpected screen transitions
- Cart-wide discount anomalies

---

### 2. Barcode Swap + SCO Weight Failures
Signals:
- Weight mismatch
- SKU-to-department mismatch
- Repeated voids

---

### 3. RFID Tampering + POS Price Mismatch
Signals:
- Oversized EPC reads
- ESL price changes
- Receipt department mismatch

---

### 4. ESL Spoofing + RF Packet Storms
Signals:
- ESL updates outside schedule
- 2.4GHz packet flooding
- Price changes across multiple shelves

---

### 5. IoT Hijacking + Fallback AP Activation
Signals:
- RF interference
- IoT device resets
- Open AP mode detected

---

## SOC Action
Use correlated anomalies to:
- Prioritize incidents
- Identify multi-vector attacks
- Trigger containment workflows
- Deploy honeytokens strategically

**Related Docs:**  
- **[Incident Response](ca://s?q=Build_incident_response_docs)**  
- **[Hardening Checklist](ca://s?q=Build_hardening_docs)**
