# Electronic Shelf Label (ESL) Threat Model

## Overview
ESLs use 2.4GHz broadcast packets to update prices.  
Many systems do not sign packets or authenticate controllers.

---

## How ESL Systems Work
- ESL controller broadcasts price updates.
- Labels receive updates via 2.4GHz.
- Labels display new price instantly.

---

## Attack Classes (Conceptual Only)
### 1. Price Injection
Broadcast fake price updates.

### 2. ESL Spoofing
Impersonate ESL controller.

### 3. Packet Flooding
Overwhelm ESL network to force fallback behavior.

### 4. Unauthorized ESL Pairing
Force labels to pair with rogue controllers.

---

## Why ESLs Are Vulnerable
- Unsigned packets.
- No mutual authentication.
- Broadcast-based communication.
- No RF monitoring.
- Predictable packet structures.

---

## Defensive Notes
- Require signed ESL packets.
- Enforce controller authentication.
- Monitor ESL update schedules.
- Deploy ESL honeytokens.

**Related:** [ESL Spoofing Detection](ca://s?q=Explain_pattern_driven_targeting)
