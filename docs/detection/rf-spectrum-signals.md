# RF Spectrum Detection Signals

## Purpose
Detect RF-based attacks across 13.56MHz, UHF RFID, and 2.4GHz IoT/ESL bands.

## Key Detection Signals

### 1. Unknown Transmitters
Any RF device not in inventory:
- Rogue scanners
- Unauthorized ESL controllers
- IoT spoofing devices

---

### 2. High-Power Bursts
Indicates:
- RF jamming
- Interference attacks
- Reader destabilization

---

### 3. Packet Storms
Occurs when:
- ESL packets flood the channel
- IoT devices are spammed
- Attackers brute-force pairing

---

### 4. Malformed Frames
Examples:
- Invalid CRC
- Oversized packets
- Illegal opcodes

---

### 5. Rapid Tag Reads
Indicates:
- RFID cloning
- Inventory scraping
- Rogue reader activity

---

### 6. Fallback AP Activation
IoT devices entering:
- Setup mode
- Open AP mode
- Pairing mode

Investigate via:  
**[IoT broadcast hijacking](ca://s?q=Explain_pattern_driven_targeting)**
