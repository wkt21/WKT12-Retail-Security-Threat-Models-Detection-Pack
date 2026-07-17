# Step 1 — Identify the Event

## Purpose
The first step in retail incident response is to **identify the event** and collect all relevant data before containment.

## Data to Collect
- Terminal ID
- Cashier ID
- SKU and product description
- Coupon code or discount ID
- HID device ID
- RFID/ESL reader logs
- Time and location of event

## Indicators of Suspicion
- Unusual void or override rates
- Cart-wide discounts from product coupons
- Scan-to-total time anomalies
- Repeated same-item voids
- ESL price updates outside schedule

## SOC Actions
- Flag the transaction in the POS log.
- Preserve raw HID input data.
- Capture RF spectrum snapshot if applicable.
- Notify LP and store management.

**Related Docs:** [Detection Signals](ca://s?q=Build_detection_docs)
