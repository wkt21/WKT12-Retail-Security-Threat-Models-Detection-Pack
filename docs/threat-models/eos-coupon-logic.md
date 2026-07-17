# EOS Coupon Logic Manipulation Threat Model

## Concept
Attackers encode **cart-wide discounts** inside **product-level coupons** to exploit weak POS discount logic.

## Attack Flow
1. Coupon appears to offer 5% off a product.
2. QR/HID input contains malformed discount logic.
3. POS applies 50% off total cart.
4. Fraud completes.

## Why It Works
- Coupon parser trusts input.
- No coupon format validation.
- No discount-range enforcement.
- No workflow integrity checks.

## Defensive Notes
- Validate coupon format and length.
- Enforce discount ranges per category.
- Bind coupons to specific SKUs.
- Monitor discount overrides and void rates.

**Related Docs:** [Incident Response](ca://s?q=Build_incident_response_docs)
