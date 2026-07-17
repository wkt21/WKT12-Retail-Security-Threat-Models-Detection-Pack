# RF Spectrum Monitoring Playbook

## Overview
RF attacks succeed because SOCs rarely monitor RF.  
This playbook defines how to detect anomalies across 13.56MHz, UHF RFID, and 2.4GHz ESL/IoT bands.

---

## RF Bands to Monitor
- 13.56MHz (HF RFID)
- 860–960MHz (UHF RFID)
- 2.4GHz (ESL, IoT, BLE, Zigbee)

---

## Detection Signals

### 1. Unknown Transmitters
Any RF device not in inventory.

### 2. High-Power Bursts
Indicates jamming or interference.

### 3. Packet Storms
Indicates ESL spoofing or brute forcing.

### 4. Malformed Frames
Invalid CRC, oversized packets, illegal opcodes.

### 5. Rapid Tag Reads
Indicates cloning or scraping.

### 6. Fallback AP Activation
IoT devices entering insecure pairing modes.

---

## SOC Response Workflow
1. Identify RF source.
2. Check reader logs.
3. Inspect ESL update logs.
4. Capture RF snapshot.
5. Locate physical device.
6. Disable rogue transmitter.
7. Update RF rules.
8. Deploy honeytokens.

**Related:** [RFID Honeytokens](ca://s?q=Show_me_honeytoken_input_patterns)
