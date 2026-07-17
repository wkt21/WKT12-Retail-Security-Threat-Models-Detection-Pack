# Scanner Hardening Guide

Retail barcode scanners are the first line of defense.  
Most attacks begin with HID/QR injection or scanner misconfiguration.

---

## 1. Disable HID Mode
HID mode allows scanners to act like keyboards.  
Disable it unless absolutely required.

**Related:** [HID threat model](ca://s?q=Help_me_build_a_threat_model_for_QR_HID_attacks)

---

## 2. Disable “Programming Mode” Barcodes
Attackers use configuration barcodes to:
- Enable HID mode
- Change prefix/suffix behavior
- Enable multi-line input

Disable all programming barcodes except those used by authorized technicians.

---

## 3. Disable Auto-Enter / Auto-Tab
Auto-enter allows attackers to:
- Trigger workflow transitions
- Escape POS screens
- Apply discounts automatically

Disable auto-enter and auto-tab globally.

---

## 4. Enforce Serial-Only Mode
Serial mode:
- Prevents HID injection
- Forces scanners to send raw data only
- Allows POS to validate input before processing

---

## 5. Restrict Multi-Line Input
Multi-line input enables:
- QR-based payloads
- Workflow escape
- Discount logic manipulation

Allow only single-line input.

---

## 6. Firmware Update Posture
Ensure:
- Latest firmware
- Vendor security patches
- Disabled legacy compatibility modes

---

## 7. Scanner Inventory Control
Track:
- Serial numbers
- MAC addresses
- Assigned terminals

Unauthorized scanners = immediate red flag.

