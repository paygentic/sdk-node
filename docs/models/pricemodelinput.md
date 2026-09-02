# PriceModelInput

Pricing model accepted when creating or updating a price. 'standard' takes a single rate in properties.unitPrice; 'volume' takes a ladder of bands in properties.tiers. Percentage-style and revenue-share pricing are expressed with 'standard' plus a unit-price multiplier (e.g. 10% ⇒ unitPrice '0.1'). The legacy 'dynamic' and 'percentage' models remain billable and readable on existing prices but can no longer be created.

## Example Usage

```typescript
import { PriceModelInput } from "@paygentic/sdk/models";

let value: PriceModelInput = "standard";
```

## Values

```typescript
"standard" | "volume"
```