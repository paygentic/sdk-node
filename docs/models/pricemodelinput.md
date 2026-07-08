# PriceModelInput

Pricing model accepted when creating or updating a price. Only 'standard' is creatable. Percentage-style and revenue-share pricing are expressed with 'standard' plus a unit-price multiplier (e.g. 10% ⇒ unitPrice '0.1'). The legacy 'dynamic', 'volume', and 'percentage' models remain billable and readable on existing prices but can no longer be created.

## Example Usage

```typescript
import { PriceModelInput } from "@paygentic/sdk/models";

let value: PriceModelInput = "standard";
```

## Values

```typescript
"standard"
```