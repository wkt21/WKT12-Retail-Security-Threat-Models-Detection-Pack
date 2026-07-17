# Self-Checkout Detection Signals

## Purpose
Detect fraud, label tampering, and HID/QR injection at self-checkout lanes.

## Key Detection Signals

### 1. Weight-Verification Failures
Triggers:
- Wrong item placed in bagging area
- Barcode swap fraud
- Hidden high-value items

---

### 2. Item-Not-Found Loops
Repeated “item not found” errors indicate:
- Counterfeit barcodes
- Invalid SKU ranges
- HID injection bypassing SKU lookup

---

### 3. Multiple Scans of the Same Item
Patterns:
- Same SKU scanned 3–10 times rapidly
- High-value SKU voided repeatedly

Indicates workflow manipulation.

---

### 4. Unusually Fast Scan Cadence
If scan cadence exceeds human capability:
- HID injection
- QR-based automation
- Rogue scanner behavior

Investigate via: **[HID anomaly detection](ca://s?q=How_to_detect_anomalous_HID_input_patterns)**

---

### 5. Unexpected “Scan Again” Prompts
Often caused by:
- Malformed barcodes
- Oversized QR payloads
- Scanner programming mode activation

---

### 6. SCO Terminal Mode Changes
Examples:
- SCO enters attendant mode without input
- SCO jumps to payment screen prematurely

Indicates workflow escape or HID injection.
