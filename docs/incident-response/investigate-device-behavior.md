# Step 3 — Investigate Device Behavior

## Purpose
Determine whether the scanner, RFID reader, or ESL controller behaved abnormally during the event.

## Investigation Checklist
- HID input anomalies
- Rogue scanner detection
- Modifier key attempts
- Oversized EPC reads
- ESL update anomalies
- RF interference or packet storms

## SOC Actions
- Review scanner configuration logs.
- Check for unauthorized HID devices.
- Inspect RF spectrum data for anomalies.
- Validate ESL update timestamps.
- Identify any firmware mismatches.

**Related Docs:** [RF Spectrum Monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
