# RFID Threat Model

## Overview
RFID systems in retail environments are widely deployed but rarely secured.  
Most tags lack authentication, use writable memory blocks, and rely on readers that trust tag data blindly.

---

## How RFID Works (Conceptual)
- Reader emits RF field.
- Passive tag powers up.
- Tag returns stored data (SKU, price, ID).
- POS or inventory system trusts the returned data.

---

## Attack Classes (Conceptual Only)
### 1. Tag Rewriting
Attackers modify:
- SKU
- Price
- Product category

### 2. Tag Cloning
Duplicate a legitimate tag onto a blank tag.

### 3. EPC Fuzzing
Send oversized or malformed EPC frames to destabilize readers.

### 4. Reader Spoofing
Impersonate legitimate readers to push malicious updates.

---

## Why RFID Is Vulnerable
- No authentication on tags.
- Writable memory blocks.
- Readers accept oversized EPC frames.
- No RF spectrum monitoring.
- POS trusts tag data without validation.

---

## Defensive Notes
- Lock writable blocks.
- Enforce reader authentication.
- Validate EPC length and CRC.
- Monitor RF anomalies.

**Related:** [RF Spectrum Monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
