# POS Behavioral Detection Signals

## Purpose
Identify anomalous POS activity that indicates HID/QR injection, coupon manipulation, barcode fraud, or workflow abuse.

## Key Detection Signals

### 1. Anomalous Void/Override Rates
Repeated voids or overrides on specific SKUs indicate:
- Price substitution attempts
- HID injection
- Coupon logic manipulation

Investigate via: **[Contextual HID anomalies](ca://s?q=Detect_contextual_HID_anomalies)**

---

### 2. Repeated Same-Item High-Value Voids
Patterns include:
- Multiple voids of the same expensive SKU
- Voids immediately followed by cheaper SKU scans

This is a classic barcode-swap fraud indicator.

---

### 3. Price Mismatches Between Receipt Description and Department
Examples:
- Electronics SKU scanned as “Grocery”
- Apparel SKU scanned as “Household”

Indicates label tampering or counterfeit barcodes.

---

### 4. Scan-to-Total Time Anomalies
If checkout time is **too fast**, it suggests:
- HID injection
- QR-based workflow escape
- Automated input instead of human scanning

---

### 5. Discount Applied Outside Coupon Workflow
Examples:
- Cart-wide discount triggered by product coupon
- Discount applied without coupon scan

Indicates coupon logic manipulation.

---

### 6. Unexpected POS Workflow Transitions
Signals:
- Jumping from scan screen → total screen
- Entering discount mode without cashier input

Investigate via: **[POS workflow integrity](ca://s?q=How_to_add_POS_workflow_integrity_checks)**
