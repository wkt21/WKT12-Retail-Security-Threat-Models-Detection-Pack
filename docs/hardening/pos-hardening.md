# POS Hardening Guide

POS terminals are the core of retail security.  
Hardening them prevents workflow escape, discount manipulation, and HID injection.

---

## 1. HID Input Allowlisting
Allow only:
- Digits 0–9
- A–Z (uppercase)
- Limited punctuation

Block:
- Modifier keys
- Escape sequences
- Multi-character payloads

**Related:** [HID anomaly detection](ca://s?q=How_to_detect_anomalous_HID_input_patterns)

---

## 2. Keyboard-Focus Restrictions
Ensure:
- Scanner input cannot change focus
- POS fields cannot be selected via HID
- Discount fields require manual cashier input

---

## 3. Coupon Format Validation
Validate:
- Length
- Character set
- Prefix/suffix
- Category binding

Reject malformed coupons automatically.

---

## 4. Discount-Range Enforcement
Examples:
- Product coupons max 5–20%
- Cart-wide discounts require manager approval

Prevents EOS coupon logic manipulation.

---

## 5. SKU-to-Department Binding
If SKU department ≠ scanned department:
- Flag transaction
- Require override
- Log anomaly

Prevents barcode swap fraud.

---

## 6. Price-Range Enforcement
If price is outside expected range:
- Trigger alert
- Require manager approval

---

## 7. Workflow Integrity Checks
Detect:
- Unexpected screen transitions
- Rapid scan-to-total jumps
- Discount mode activation without cashier input

**Related:** [POS workflow integrity](ca://s?q=How_to_add_POS_workflow_integrity_checks)
