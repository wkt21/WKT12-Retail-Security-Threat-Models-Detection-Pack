# Pattern-Driven Targeting Threat Model

## Concept
Attackers follow predictable patterns in technology, human behavior, and retail workflows rather than random targets.

## Attack Flow
1. Identify predictable weaknesses (self-checkout, EOS sales, busy hours).
2. Exploit POS logic or RF environment.
3. Trigger fraud or injection event.
4. Evade detection through normal workflows.

## Why It Works
- SOCs focus on high-profile cyber threats.
- Retail workflows are predictable.
- RF environments are noisy and unmonitored.
- Staff behavior is consistent.

## Defensive Notes
- Deploy honeytokens where patterns predict attacks.
- Build detection rules based on workflow anomalies.
- Harden systems against predictable weaknesses.
- Train staff on pattern recognition.

**Related Docs:** [Detection Signals](ca://s?q=Build_detection_docs)
