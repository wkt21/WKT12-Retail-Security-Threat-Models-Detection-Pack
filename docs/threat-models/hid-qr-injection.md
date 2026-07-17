# HID / QR Injection Threat Model

## Concept
Retail scanners often operate in **HID (Human Interface Device)** mode, meaning they act like keyboards.  
Attackers exploit this by encoding **multi-character input** in QR codes or barcodes that the POS interprets as commands.

## Attack Flow
1. Attacker prints a malicious QR or barcode.
2. Scanner reads it as keyboard input.
3. POS interprets the input as workflow commands.
4. Price manipulation or discount override occurs.

## Why Scanners Are Vulnerable
- HID mode enabled by default.
- “Programming mode” barcodes not disabled.
- No input sanitization.
- No SKU binding.
- No discount-range enforcement.

## Defensive Notes
- Disable HID mode.
- Enforce serial-only communication.
- Validate input length and character set.
- Monitor scan-to-total time anomalies.

**Related Docs:** [Detection Signals](ca://s?q=Build_detection_docs)
