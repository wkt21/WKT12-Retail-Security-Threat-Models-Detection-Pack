# RF Replay Attacks

## Overview
RF replay attacks involve capturing legitimate RF signals and replaying them later to trigger unauthorized actions.

---

## Replayable Signals (Conceptual)
- Unlock signals
- On/off commands
- Automation triggers
- ESL price updates
- RFID reader commands

---

## Attack Flow
1. Attacker captures RF signal.
2. Stores signal using SDR or RF tool.
3. Replays signal at a later time.
4. Device performs the action without authentication.

---

## Why Replay Works
- No rolling codes
- No timestamp validation
- No mutual authentication
- Predictable RF patterns

---

## Detection Signals
- Duplicate RF commands
- Commands outside normal schedule
- Repeated identical packets
- RF bursts without device activity

---

## Defensive Notes
- Use rolling codes
- Enforce signed RF packets
- Monitor RF replay patterns
- Deploy RF honeytokens

**Related:** [RF Spectrum Signals](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
