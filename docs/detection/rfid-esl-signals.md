# RFID & ESL Detection Signals

## Purpose
Detect manipulation of RFID tags, electronic shelf labels (ESLs), and RF-based price systems.

## Key Detection Signals

### 1. Oversized EPC Reads
Normal EPC = 96 bits  
Oversized EPC = 256–512 bits  
Indicates:
- Fuzzing
- Rogue tag
- Reader misconfiguration

---

### 2. Malformed RFID Frames
Examples:
- Invalid CRC
- Illegal characters
- Multi-block responses

Investigate via: **[RFID threat model](ca://s?q=Explain_misconfiguration_exploitation)**

---

### 3. Unknown Reader IDs
Signals:
- Rogue handheld readers
- Unauthorized inventory devices
- Spoofed reader MAC addresses

---

### 4. ESL Price Updates Outside Schedule
Indicates:
- ESL spoofing
- 2.4GHz broadcast injection
- Rogue ESL controller

---

### 5. Unauthorized Write Attempts
Occurs when:
- Writable tag blocks are accessed
- ESL packets attempt price changes
- Reader logs show write commands

---

### 6. 2.4GHz Packet Storms
Indicates:
- RF interference attacks
- ESL broadcast flooding
- IoT hijacking attempts

Investigate via: **[RF spectrum monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)**
