# RFID / ESL Manipulation Threat Model

## Concept
RFID tags and electronic shelf labels (ESLs) often lack authentication, allowing attackers to rewrite or spoof data.

## Attack Flow
1. Attacker uses 13.56MHz or 2.4GHz tools.
2. Rewrites tag or injects ESL price update.
3. POS or shelf displays incorrect price.
4. Fraud or inventory manipulation occurs.

## Why It Works
- Unauthenticated tags.
- Writable memory blocks.
- ESL packets not signed.
- No RF spectrum monitoring.

## Defensive Notes
- Lock writable tag blocks.
- Require signed ESL packets.
- Enforce reader authentication.
- Monitor RF spectrum for anomalies.

**Related Docs:** [RF Spectrum Monitoring](ca://s?q=Design_a_SOC_playbook_for_HID_honeytoken_alerts)
