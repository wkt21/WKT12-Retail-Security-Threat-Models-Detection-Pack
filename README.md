# WKT12-Retail-Security-Threat-Models-Detection-Pack

<img width="1536" height="1024" alt="IMG_2131" src="https://github.com/user-attachments/assets/66445691-5b29-4467-8abe-869ccb190755" />


A comprehensive, research‑driven documentation suite covering barcode/QR/HID injection, RFID/ESL manipulation, swap fraud, and POS logic abuse. Designed for SOC analysts, Loss Prevention teams, retail security engineers, and researchers building modern defenses against overlooked but high‑impact retail attack surfaces.

Designed for SOC analysts, Loss Prevention teams, retail security engineers, and researchers building modern defenses against overlooked but high‑impact retail attack surfaces.

This repo contains no exploit code, no payloads, and no harmful instructions — only conceptual threat models, detection signals, hardening guidance, and incident‑response playbooks.

---

📂 Repository Structure

/README.md
/docs/
    /threat-models/
    /detection/
    /hardening/
    /incident-response/
    /rfid-esl/
    /iot-rf/
    /patterns/
/diagrams/


Each folder contains Markdown documentation designed for real‑world retail SOC/LP use.

---

🔎 Overview

Retail environments are uniquely vulnerable because they rely on:

• HID‑mode barcode scanners
• QR‑based coupons
• RFID tags with no authentication
• Electronic shelf labels (ESLs) using 2.4GHz broadcast packets
• IoT devices with insecure fallback modes
• Legacy POS systems with weak input validation


These systems create low‑skill, high‑impact attack surfaces that are rarely monitored by traditional SOCs.

This repo documents how these attacks work conceptually, how to detect them, how to harden systems, and how to respond.

---

📘 1. Threat Models

Conceptual explanations of how each attack class works — no payloads, no exploit code, only defensive research.

HID / QR Injection

Scanners behave like keyboards → POS trusts HID input → malformed QR codes can escape workflows.

Barcode Swap Fraud

Counterfeit labels placed on products → POS trusts scanned SKU → price mismatch.

EOS Coupon Logic Manipulation

Malformed coupons override discount logic → cart‑wide discounts applied from product coupons.

RFID / ESL Manipulation

Unauthenticated tags + unsigned ESL packets → price manipulation, inventory tampering.

Pattern‑Driven Targeting

Attackers follow predictable patterns in POS workflows, RF environments, and human behavior.

Full docs:

• HID/QR threat model
• Barcode fraud modeling
• Coupon logic threat model
• RFID/ESL threat model
• Pattern‑driven targeting


---

📡 2. Detection Signals

Real, measurable indicators that SOC/LP teams should alert on.

POS Behavioral Signals

• Anomalous void/override rates
• Repeated voids on same high‑value SKU
• Price mismatches between receipt description and department
• Scan‑to‑total time anomalies
• Cart‑wide discount triggered by product coupon


Self‑Checkout Signals

• Weight‑verification failures
• Item‑not‑found loops
• Multiple scans of same item
• Unusually fast scan cadence


RFID / ESL Signals

• Oversized EPC reads
• Malformed RFID frames
• Unknown reader IDs
• ESL price updates outside schedule
• 2.4GHz packet storms


Full docs:

• HID anomaly detection
• RF anomaly detection


---

🛡️ 3. Hardening Checklist

Operational controls retailers must implement.

Scanner Hardening

• Disable HID mode
• Disable “programming mode” barcodes
• Disable auto‑enter
• Enforce serial‑only mode


POS Hardening

• HID input allowlisting
• Coupon format validation
• Discount‑range enforcement
• SKU‑to‑department binding
• Workflow integrity checks


RFID / ESL Hardening

• Lock writable tag blocks
• Require signed ESL packets
• Enforce reader authentication
• RF spectrum monitoring


Physical Controls

• Label‑stock control
• Tamper‑evident labels
• Randomized SCO audits


Full docs:

• Scanner lockdown
• POS workflow integrity


---

🚨 4. Incident Response Playbook

What SOC/LP teams should do once swap fraud or injection attempts are suspected.

Step 1 — Identify

Collect terminal ID, cashier ID, SKU, coupon code, HID device ID, RFID/ESL logs.

Step 2 — Validate

Check expected vs actual price, discount, SKU ↔ department match.

Step 3 — Investigate

Look for HID anomalies, rogue scanners, oversized EPC reads, ESL anomalies.

Step 4 — Interview

Ask staff about coupon legitimacy, customer behavior, scanner issues.

Step 5 — Contain

Disable scanner, lock POS, remove counterfeit labels, freeze coupons.

Step 6 — Correct

Update scanner config, coupon parser, deploy honeytokens, add RF rules.

Step 7 — Document

Root cause, impact, controls added, staff retraining.

Full docs:

• IR playbook


---

📡 5. RFID & ESL Modules

Includes:

• RFID honeytoken design
• ESL spoofing threat model
• RF spectrum monitoring playbook
• 2.4GHz interference → IoT fallback → takeover chain


Full docs:

• RFID honeytokens
• RF spectrum monitoring


---

📘 6. IoT & RF Modules

Includes:

• IoT broadcast hijacking
• BLE/Zigbee pairing exploitation
• Fallback AP takeover
• RF replay modeling


Full docs:

• IoT broadcast hijacking


---

📄 License

MIT License (recommended for research repos).

---

🤝 Contributing

Pull requests welcome.
All contributions must remain defensive, non‑exploitative, and research‑focused.
