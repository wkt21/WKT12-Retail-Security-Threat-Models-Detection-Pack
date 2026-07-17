# ESL Spoofing Detection

## Overview
ESL spoofing is one of the most damaging retail RF attacks.  
Attackers inject fake price updates or impersonate ESL controllers.

---

## Detection Signals

### 1. ESL Price Updates Outside Schedule
Indicates:
- Rogue controller
- Broadcast injection

---

### 2. Unknown ESL Controller IDs
Signals:
- Spoofed MAC addresses
- Unauthorized devices

---

### 3. 2.4GHz Packet Storms
Indicates:
- Flooding attacks
- ESL destabilization attempts

---

### 4. Price Changes Across Multiple Shelves
If multiple ESLs change simultaneously:
- Controller compromise
- Broadcast spoofing

---

### 5. ESL Pairing Attempts
Labels attempting to pair with unknown controllers.

---

## SOC Actions
- Capture RF spectrum snapshot.
- Identify controller MAC.
- Validate ESL update logs.
- Lock down ESL network segment.

**Related:** [RF Spectrum Signals](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
