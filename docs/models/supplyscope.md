# SupplyScope

Whether this price's money is consideration for a supply — the one tax fact only you can state, because it is settled when you agree the deal rather than derived from what was sold. `IN_SCOPE` (the default) is consideration: it enters the taxable amount, positive as a charge or negative as a reduction in the price of the supply it applies to. `OUTSIDE_SCOPE` money is not consideration for anything, so it does not change the taxable amount, carries no tax, does not appear on the tax document, and nets into the amount payable after tax. This means "not consideration for a supply" — it does NOT mean "a supply outside this jurisdiction": exports and place-of-supply answers are worked out from the addresses on the sale by the tax provider, and are never declared on a price. How a supply is then classified — standard, zero-rated, exempt — is the tax provider's determination and is not set here either. Omit the whole `tax` object to leave a price in scope; there is deliberately no schema default on this property, so that a misspelt key is refused rather than silently defaulted.

## Example Usage

```typescript
import { SupplyScope } from "@paygentic/sdk/models";

let value: SupplyScope = "OUTSIDE_SCOPE";
```

## Values

```typescript
"IN_SCOPE" | "OUTSIDE_SCOPE"
```