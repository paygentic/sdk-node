# OutsideScopeLabel

What an `OUTSIDE_SCOPE` amount is called in the invoice totals, so the wording follows the declaration rather than being retyped per price. Required when `supplyScope` is `OUTSIDE_SCOPE`, and rejected otherwise. `CASHBACK` is the only value today, and a price declaring it must use the `standard` model and must not carry a positive `unitPrice` — a cashback is money paid back, not charged.

## Example Usage

```typescript
import { OutsideScopeLabel } from "@paygentic/sdk/models";

let value: OutsideScopeLabel = "CASHBACK";
```

## Values

```typescript
"CASHBACK"
```