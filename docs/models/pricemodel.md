# PriceModel

Pricing model of a price as returned by the API. Includes the legacy models ('dynamic', 'percentage') retained for existing prices; 'standard' and 'volume' can be created (see PriceModelInput).

## Example Usage

```typescript
import { PriceModel } from "@paygentic/sdk/models";

let value: PriceModel = "volume";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"standard" | "dynamic" | "volume" | "percentage" | Unrecognized<string>
```