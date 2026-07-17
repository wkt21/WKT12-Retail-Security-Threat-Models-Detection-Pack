# RFID & ESL Hardening Guide

RFID tags and ESL systems are extremely powerful — and extremely vulnerable without proper controls.

---

## 1. Lock Writable Tag Blocks
Prevent:
- SKU rewriting
- Price manipulation
- Inventory tampering

---

## 2. Require Signed ESL Packets
Unsigned packets allow:
- Price injection
- Rogue controller spoofing
- Broadcast hijacking

Sign all ESL updates cryptographically.

---

## 3. Enforce Reader Authentication
Readers must:
- Authenticate to backend
- Use signed commands
- Reject oversized EPC frames

---

## 4. RF Spectrum Monitoring
Monitor:
- 13.56MHz (HF RFID)
- UHF RFID
- 2.4GHz (ESL, IoT)

Detect:
- Packet storms
- Rogue transmitters
- Malformed frames

**Related:** [RF spectrum monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)

---

## 5. ESL Update Scheduling
Only allow ESL updates:
- During maintenance windows
- From authenticated controllers
- With signed packets

---

## 6. Reader Whitelisting
Whitelist:
- Reader MAC addresses
- Reader serial numbers
- Reader locations

Unknown reader = immediate alert.

