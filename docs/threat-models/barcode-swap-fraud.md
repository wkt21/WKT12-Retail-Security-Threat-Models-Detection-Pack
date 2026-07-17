# Barcode Swap Fraud Threat Model

## Concept
Attackers replace legitimate product labels with counterfeit barcodes representing cheaper SKUs.

## Attack Flow
1. Attacker prints a low-value SKU barcode.
2. Places it over a high-value item.
3. POS trusts the scanned SKU.
4. Price mismatch results in loss.

## Why It Works
- No label-stock control.
- No SKU-to-department validation.
- No price-range enforcement.
- Staff rarely inspect labels.

## Defensive Notes
- Implement SKU-to-department binding.
- Enforce price-range validation.
- Train staff to recognize counterfeit labels.
- Audit self-checkout lanes for label tampering.

**Related Docs:** [Hardening Checklist](ca://s?q=Build_hardening_docs)
