# Network Segmentation Guide

Segmentation prevents IoT compromise from pivoting into POS, ESL, or corporate networks.

---

## 1. Separate IoT from POS
IoT devices must never share:
- VLANs
- Subnets
- Authentication domains

---

## 2. ESL Network Isolation
ESLs should be isolated from:
- POS terminals
- Corporate Wi-Fi
- Guest Wi-Fi

---

## 3. RFID Reader Segmentation
Readers should:
- Use dedicated VLANs
- Authenticate to backend
- Log all commands

---

## 4. Guest Wi-Fi Isolation
Guest Wi-Fi must:
- Never touch POS
- Never touch IoT
- Never touch ESL

---

## 5. Fallback AP Detection
Monitor for:
- IoT devices broadcasting SSIDs
- Unexpected APs
- RF interference preceding AP activation

**Related:** [Fallback AP takeover](ca://s?q=Explain_pattern_driven_targeting)
