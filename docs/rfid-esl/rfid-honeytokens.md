# RFID Honeytoken Design

## Overview
RFID honeytokens are decoy tags engineered to detect tampering, fuzzing, cloning, and unauthorized readers.

---

## Honeytoken Types

### 1. Oversized EPC Honeytokens
Normal EPC: 96 bits  
Honeytoken EPC: 256–512 bits  
If accepted → reader misconfiguration.

---

### 2. Illegal Character Honeytokens
Insert characters that should never appear:
`! @ # $ % ^ & *`

If accepted → reader lacks validation.

---

### 3. Unicode / RTL Honeytokens
Insert RTL markers or homoglyphs.

If accepted → encoding flaw.

---

### 4. Multi-Block Response Honeytokens
Tag responds with multiple blocks even when one is requested.

If processed → reader vulnerable to fuzzing.

---

### 5. Writable-Block Honeytokens
Writable blocks that should be locked.

If written → insider or rogue device.

---

## Deployment Strategy
Place honeytokens:
- Inventory bins
- Warehouse intake stations
- ESL shelves
- POS backrooms
- Return counters

---

## SOC Alerts
- Oversized EPC reads
- Illegal characters
- Multi-block responses
- Unauthorized write attempts
- Unknown reader IDs

**Related:** [RFID Threat Model](ca://s?q=Explain_misconfiguration_exploitation)
